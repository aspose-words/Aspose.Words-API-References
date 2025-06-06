---
title: DocumentBuilder.EndEditableRange
linktitle: EndEditableRange
articleTitle: EndEditableRange
second_title: Aspose.Words för .NET
description: Upptäck DocumentBuilder-metoden EndEditableRange för att effektivt markera redigerbara avsnitt i dina dokument och förbättra ditt redigeringsarbetsflöde.
type: docs
weight: 230
url: /sv/net/aspose.words/documentbuilder/endeditablerange/
---
## EndEditableRange() {#endeditablerange}

Markerar den aktuella positionen i dokumentet som ett redigerbart områdesslut.

```csharp
public EditableRangeEnd EndEditableRange()
```

### Returvärde

Den redigerbara intervallslutnoden som just skapades.

## Anmärkningar

Redigerbart område i ett dokument kan överlappa och omfatta vilket område som helst. För att skapa ett giltigt redigerbart område måste du anropa båda.[`StartEditableRange`](../starteditablerange/) och`EndEditableRange` eller`EndEditableRange` metoder.

Felaktigt utformade redigerbara områden kommer att ignoreras när dokumentet sparas.

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

* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## EndEditableRange(*[EditableRangeStart](../../editablerangestart/)*) {#endeditablerange_1}

Markerar den aktuella positionen i dokumentet som ett redigerbart områdesslut.

```csharp
public EditableRangeEnd EndEditableRange(EditableRangeStart start)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| start | EditableRangeStart | Detta redigerbara intervall börjar. |

### Returvärde

Den redigerbara intervallslutnoden som just skapades.

## Anmärkningar

Använd denna överbelastning när du skapar kapslade redigerbara områden.

Redigerbart område i ett dokument kan överlappa och omfatta vilket område som helst. För att skapa ett giltigt redigerbart område måste du anropa båda.[`StartEditableRange`](../starteditablerange/) och`EndEditableRange` eller`EndEditableRange` metoder.

Felaktigt utformade redigerbara områden kommer att ignoreras när dokumentet sparas.

## Exempel

Visar hur man skapar kapslade redigerbara områden.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Skapa två kapslade redigerbara områden.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// För närvarande finns dokumentbyggarens nodinsättningsmarkör i mer än ett pågående redigerbart område.
// När vi vill avsluta ett redigerbart område i den här situationen,
// vi måste ange vilket av intervallen vi vill avsluta genom att skicka dess EditableRangeStart-nod.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Om ett textområde har två överlappande redigerbara områden med angivna grupper,
// den kombinerade gruppen av användare som exkluderas av båda grupperna hindras från att redigera den.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

### Se även

* class [EditableRangeEnd](../../editablerangeend/)
* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
