---
title: EndEditableRange
second_title: Aspose.Words för .NET API Referens
description: Markerar den aktuella positionen i dokumentet som ett redigerbart intervallslut.
type: docs
weight: 210
url: /sv/net/aspose.words/documentbuilder/endeditablerange/
---
## EndEditableRange() {#endeditablerange}

Markerar den aktuella positionen i dokumentet som ett redigerbart intervallslut.

```csharp
public EditableRangeEnd EndEditableRange()
```

### Returvärde

Den redigerbara intervallnoden som just skapades.

### Anmärkningar

Redigerbart område i ett dokument kan överlappa och sträcka sig över vilket område som helst. För att skapa ett giltigt redigerbart område måste du anropa båda[`StartEditableRange`](../starteditablerange/) och`EndEditableRange` eller[`EndEditableRange`](./endeditablerange/)metoder.

Dåligt format redigerbart område kommer att ignoreras när dokumentet sparas.

### Exempel

Visar hur man arbetar med ett redigerbart område.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Redigerbara intervall tillåter oss att lämna delar av skyddade dokument öppna för redigering.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Ett välformat redigerbart område har en startnod och en slutnod.
// Dessa noder har matchande ID:n och omfattar redigerbara noder.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Olika delar av det redigerbara intervallet länkar till varandra.
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

// Ta bort ett redigerbart område. Alla noder som fanns inom intervallet kommer att förbli intakta.
editableRange.Remove();
```

### Se även

* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

---

## EndEditableRange(EditableRangeStart) {#endeditablerange_1}

Markerar den aktuella positionen i dokumentet som ett redigerbart intervallslut.

```csharp
public EditableRangeEnd EndEditableRange(EditableRangeStart start)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| start | EditableRangeStart | Detta redigerbara intervall startar. |

### Returvärde

Den redigerbara intervallnoden som just skapades.

### Anmärkningar

Använd denna överbelastning när du skapar kapslade redigerbara intervall.

Redigerbart område i ett dokument kan överlappa och sträcka sig över vilket område som helst. För att skapa ett giltigt redigerbart område måste du anropa båda[`StartEditableRange`](../starteditablerange/) och[`EndEditableRange`](./endeditablerange/) eller`EndEditableRange`metoder.

Dåligt format redigerbart område kommer att ignoreras när dokumentet sparas.

### Exempel

Visar hur man skapar kapslade redigerbara intervall.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Skapa två kapslade redigerbara intervall.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// För närvarande är dokumentbyggarens nodinfogningsmarkör inom mer än ett pågående redigerbart område.
// När vi vill avsluta ett redigerbart intervall i den här situationen,
// vi måste ange vilket av intervallen vi vill avsluta genom att skicka dess EditableRangeStart-nod.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Om en textregion har två överlappande redigerbara intervall med specificerade grupper,
// den kombinerade gruppen av användare som utesluts av båda grupperna hindras från att redigera den.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

### Se även

* class [EditableRangeEnd](../../editablerangeend/)
* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
