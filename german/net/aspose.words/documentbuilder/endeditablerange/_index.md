---
title: DocumentBuilder.EndEditableRange
linktitle: EndEditableRange
articleTitle: EndEditableRange
second_title: Aspose.Words für .NET
description: Entdecken Sie die DocumentBuilder-Methode „EndEditableRange“, um bearbeitbare Abschnitte in Ihren Dokumenten effizient zu markieren und so Ihren Bearbeitungsworkflow zu verbessern.
type: docs
weight: 230
url: /de/net/aspose.words/documentbuilder/endeditablerange/
---
## EndEditableRange() {#endeditablerange}

Markiert die aktuelle Position im Dokument als editierbares Bereichsende.

```csharp
public EditableRangeEnd EndEditableRange()
```

### Rückgabewert

Der gerade erstellte bearbeitbare Bereichsendknoten.

## Bemerkungen

Der bearbeitbare Bereich in einem Dokument kann sich über jeden Bereich erstrecken. Um einen gültigen bearbeitbaren Bereich zu erstellen, müssen Sie beide aufrufen.[`StartEditableRange`](../starteditablerange/) Und`EndEditableRange` oder`EndEditableRange` Methoden.

Ein falsch formatierter bearbeitbarer Bereich wird beim Speichern des Dokuments ignoriert.

## Beispiele

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
// Diese Knoten haben übereinstimmende IDs und umfassen bearbeitbare Knoten.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Verschiedene Teile des bearbeitbaren Bereichs sind miteinander verknüpft.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// So können wir auf die Knotentypen jedes Teils zugreifen. Der editierbare Bereich selbst ist kein Knoten,
// sondern eine Entität, die aus einem Anfang, einem Ende und dem darin enthaltenen Inhalt besteht.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Einen bearbeitbaren Bereich entfernen. Alle Knoten innerhalb des Bereichs bleiben erhalten.
editableRange.Remove();
```

### Siehe auch

* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## EndEditableRange(*[EditableRangeStart](../../editablerangestart/)*) {#endeditablerange_1}

Markiert die aktuelle Position im Dokument als editierbares Bereichsende.

```csharp
public EditableRangeEnd EndEditableRange(EditableRangeStart start)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| start | EditableRangeStart | Dieser bearbeitbare Bereich beginnt. |

### Rückgabewert

Der gerade erstellte bearbeitbare Bereichsendknoten.

## Bemerkungen

Verwenden Sie diese Überladung beim Erstellen verschachtelter bearbeitbarer Bereiche.

Der bearbeitbare Bereich in einem Dokument kann sich über jeden Bereich erstrecken. Um einen gültigen bearbeitbaren Bereich zu erstellen, müssen Sie beide aufrufen.[`StartEditableRange`](../starteditablerange/) Und`EndEditableRange` oder`EndEditableRange` Methoden.

Ein falsch formatierter bearbeitbarer Bereich wird beim Speichern des Dokuments ignoriert.

## Beispiele

Zeigt, wie verschachtelte bearbeitbare Bereiche erstellt werden.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Erstellen Sie zwei verschachtelte bearbeitbare Bereiche.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Derzeit befindet sich der Knoteneinfügecursor des Dokumentgenerators in mehr als einem laufenden bearbeitbaren Bereich.
// Wenn wir in dieser Situation einen bearbeitbaren Bereich beenden möchten,
// Wir müssen angeben, welchen der Bereiche wir beenden möchten, indem wir seinen EditableRangeStart-Knoten übergeben.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Wenn ein Textbereich zwei überlappende bearbeitbare Bereiche mit angegebenen Gruppen hat,
// Die kombinierte Gruppe von Benutzern, die von beiden Gruppen ausgeschlossen sind, kann es nicht bearbeiten.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

### Siehe auch

* class [EditableRangeEnd](../../editablerangeend/)
* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
