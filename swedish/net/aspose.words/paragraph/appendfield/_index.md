---
title: Paragraph.AppendField
second_title: Aspose.Words för .NET API Referens
description: Paragraph metod. Lägger till ett fält i detta stycke.
type: docs
weight: 240
url: /sv/net/aspose.words/paragraph/appendfield/
---
## AppendField(FieldType, bool) {#appendfield}

Lägger till ett fält i detta stycke.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldType | FieldType | Typen av fält som ska läggas till. |
| updateField | Boolean | Anger om fältet ska uppdateras omedelbart. |

### Returvärde

A[`Field`](../../../aspose.words.fields/field/) objekt som representerar det bifogade fältet.

### Exempel

Visar olika sätt att lägga till fält till ett stycke.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nedan finns tre sätt att lägga till ett fält i slutet av ett stycke.
// 1 - Lägg till ett DATUM-fält med en fälttyp och uppdatera det sedan:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - Lägg till ett TID-fält med hjälp av en fältkod: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Lägg till ett CITAT-fält med en fältkod och få det att visa ett platshållarvärde:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../paragraph/)
* hopsättning [Aspose.Words](../../../)

---

## AppendField(string) {#appendfield_1}

Lägger till ett fält i detta stycke.

```csharp
public Field AppendField(string fieldCode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | String | Fältkoden som ska läggas till (utan hängslen). |

### Returvärde

A[`Field`](../../../aspose.words.fields/field/) objekt som representerar det bifogade fältet.

### Exempel

Visar olika sätt att lägga till fält till ett stycke.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nedan finns tre sätt att lägga till ett fält i slutet av ett stycke.
// 1 - Lägg till ett DATUM-fält med en fälttyp och uppdatera det sedan:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - Lägg till ett TID-fält med hjälp av en fältkod: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Lägg till ett CITAT-fält med en fältkod och få det att visa ett platshållarvärde:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../paragraph/)
* hopsättning [Aspose.Words](../../../)

---

## AppendField(string, string) {#appendfield_2}

Lägger till ett fält i detta stycke.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | String | Fältkoden som ska läggas till (utan hängslen). |
| fieldValue | String | Fältvärdet som ska läggas till. Skicka null för fält som inte har ett värde. |

### Returvärde

A[`Field`](../../../aspose.words.fields/field/) objekt som representerar det bifogade fältet.

### Exempel

Visar olika sätt att lägga till fält till ett stycke.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nedan finns tre sätt att lägga till ett fält i slutet av ett stycke.
// 1 - Lägg till ett DATUM-fält med en fälttyp och uppdatera det sedan:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 - Lägg till ett TID-fält med hjälp av en fältkod: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Lägg till ett CITAT-fält med en fältkod och få det att visa ett platshållarvärde:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../paragraph/)
* hopsättning [Aspose.Words](../../../)


