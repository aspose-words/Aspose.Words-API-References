---
title: Paragraph.AppendField
linktitle: AppendField
articleTitle: AppendField
second_title: Aspose.Words för .NET
description: Förbättra ditt dokument med metoden Paragraph AppendField, och lägg sömlöst till anpassade fält i stycken för förbättrad organisation och tydlighet.
type: docs
weight: 260
url: /sv/net/aspose.words/paragraph/appendfield/
---
## AppendField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#appendfield}

Lägger till ett fält i detta stycke.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldType | FieldType | Typen av fält som ska läggas till. |
| updateField | Boolean | Anger om fältet ska uppdateras omedelbart. |

### Returvärde

En[`Field`](../../../aspose.words.fields/field/) objekt som representerar det tillagda fältet.

## Exempel

Visar olika sätt att lägga till fält i ett stycke.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nedan följer tre sätt att lägga till ett fält i slutet av ett stycke.
// 1 - Lägg till ett DATUM-fält med en fälttyp och uppdatera det sedan:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Lägg till ett TIME-fält med hjälp av en fältkod:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Lägg till ett QUOTE-fält med hjälp av en fältkod och få det att visa ett platshållarvärde:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Det här fältet visar sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## AppendField(*string*) {#appendfield_1}

Lägger till ett fält i detta stycke.

```csharp
public Field AppendField(string fieldCode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | String | Fältkoden som ska läggas till (utan klammerparenteser). |

### Returvärde

En[`Field`](../../../aspose.words.fields/field/) objekt som representerar det tillagda fältet.

## Exempel

Visar olika sätt att lägga till fält i ett stycke.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nedan följer tre sätt att lägga till ett fält i slutet av ett stycke.
// 1 - Lägg till ett DATUM-fält med en fälttyp och uppdatera det sedan:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Lägg till ett TIME-fält med hjälp av en fältkod:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Lägg till ett QUOTE-fält med hjälp av en fältkod och få det att visa ett platshållarvärde:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Det här fältet visar sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## AppendField(*string, string*) {#appendfield_2}

Lägger till ett fält i detta stycke.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | String | Fältkoden som ska läggas till (utan klammerparenteser). |
| fieldValue | String | Fältvärdet som ska läggas till. Pass`null` för fält som inte har ett värde. |

### Returvärde

En[`Field`](../../../aspose.words.fields/field/) objekt som representerar det tillagda fältet.

## Exempel

Visar olika sätt att lägga till fält i ett stycke.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Nedan följer tre sätt att lägga till ett fält i slutet av ett stycke.
// 1 - Lägg till ett DATUM-fält med en fälttyp och uppdatera det sedan:
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - Lägg till ett TIME-fält med hjälp av en fältkod:
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - Lägg till ett QUOTE-fält med hjälp av en fältkod och få det att visa ett platshållarvärde:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// Det här fältet visar sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
