---
title: EditableRange.EditableRangeStart
linktitle: EditableRangeStart
articleTitle: EditableRangeStart
second_title: Aspose.Words för .NET
description: Upptäck egenskapen EditableRangeStart för att komma åt noden som markerar början på ditt redigerbara område. Förbättra din redigeringsupplevelse idag!
type: docs
weight: 20
url: /sv/net/aspose.words/editablerange/editablerangestart/
---
## EditableRange.EditableRangeStart property

Hämtar noden som representerar början av det redigerbara området.

```csharp
public EditableRangeStart EditableRangeStart { get; }
```

## Exempel

Visar hur man arbetar med ett redigerbart område.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Redigerbara områden låter oss lämna delar av skyddade dokument öppna för redigering.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Ett välformat redigerbart område har en startnod och en slutnod.
// Dessa noder har matchande ID:n och omfattar redigerbara noder.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Olika delar av det redigerbara området länkar till varandra.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Vi kan komma åt nodtyperna för varje del så här. Det redigerbara området i sig är inte en nod,
// men en enhet som består av en början, ett slut och deras inneslutna innehåll.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Ta bort ett redigerbart område. Alla noder som fanns inom området kommer att förbli intakta.
editableRange.Remove();
```

### Se även

* class [EditableRangeStart](../../editablerangestart/)
* class [EditableRange](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
