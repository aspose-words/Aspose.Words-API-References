---
title: DocumentBuilder.StartEditableRange
linktitle: StartEditableRange
articleTitle: StartEditableRange
second_title: Aspose.Words für .NET
description: DocumentBuilder StartEditableRange methode. Markiert die aktuelle Position im Dokument als bearbeitbaren Bereichsstart in C#.
type: docs
weight: 630
url: /de/net/aspose.words/documentbuilder/starteditablerange/
---
## DocumentBuilder.StartEditableRange method

Markiert die aktuelle Position im Dokument als bearbeitbaren Bereichsstart.

```csharp
public EditableRangeStart StartEditableRange()
```

### Rückgabewert

Der gerade erstellte Startknoten des bearbeitbaren Bereichs.

## Bemerkungen

Der bearbeitbare Bereich in einem Dokument kann jeden Bereich überlappen und umfassen. Um einen gültigen bearbeitbaren Bereich zu erstellen, müssen Sie beide aufrufen`StartEditableRange` Und[`EndEditableRange`](../endeditablerange/) oder[`EndEditableRange`](../endeditablerange/) Methoden.

Ein fehlerhaft geformter bearbeitbarer Bereich wird beim Speichern des Dokuments ignoriert.

## Beispiele

Zeigt, wie verschachtelte bearbeitbare Bereiche erstellt werden.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Zwei verschachtelte bearbeitbare Bereiche erstellen.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Derzeit befindet sich der Knoteneinfügungscursor des Document Builders in mehr als einem fortlaufend bearbeitbaren Bereich.
// Wenn wir in dieser Situation einen bearbeitbaren Bereich beenden möchten,
// Wir müssen angeben, welchen der Bereiche wir beenden möchten, indem wir seinen EditableRangeStart-Knoten übergeben.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Wenn ein Textbereich zwei überlappende bearbeitbare Bereiche mit angegebenen Gruppen hat,
// Die kombinierte Gruppe von Benutzern, die von beiden Gruppen ausgeschlossen wurden, wird daran gehindert, es zu bearbeiten.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

Zeigt, wie mit einem bearbeitbaren Bereich gearbeitet wird.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Bearbeitbare Bereiche ermöglichen es uns, Teile geschützter Dokumente zur Bearbeitung offen zu lassen.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Ein wohlgeformter bearbeitbarer Bereich hat einen Startknoten und einen Endknoten.
// Diese Knoten haben passende IDs und umfassen bearbeitbare Knoten.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Verschiedene Teile des bearbeitbaren Bereichs sind miteinander verknüpft.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Auf diese Weise können wir auf die Knotentypen jedes Teils zugreifen. Der bearbeitbare Bereich selbst ist kein Knoten,
// sondern eine Entität, die aus einem Anfang, einem Ende und den darin enthaltenen Inhalten besteht.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Einen bearbeitbaren Bereich entfernen. Alle Knoten, die innerhalb des Bereichs lagen, bleiben intakt.
editableRange.Remove();
```

### Siehe auch

* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
