---
title: EditableRangeEnd.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words für .NET
description: Entdecken Sie die EditableRangeEnd-ID-Eigenschaft, um Ihre bearbeitbaren Bereiche einfach zu identifizieren und zu verwalten und so die Interaktivität und Kontrolle Ihres Dokuments zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words/editablerangeend/id/
---
## EditableRangeEnd.Id property

Gibt die Kennung des editierbaren Bereichs an.

```csharp
public int Id { get; set; }
```

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

* class [EditableRangeEnd](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
