---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words för .NET
description: Infoga enkelt fält i stycken med metoden Paragraph InsertField. Förbättra dokumentets funktionalitet och effektivisera innehållshanteringen.
type: docs
weight: 290
url: /sv/net/aspose.words/paragraph/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool, [Node](../../node/), bool*) {#insertfield}

Infogar ett fält i detta stycke.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldType | FieldType | Typen av fält som ska infogas. |
| updateField | Boolean | Anger om fältet ska uppdateras omedelbart. |
| refNode | Node | Referensnod i detta stycke (om*refNode* är`null`, lägger sedan till i slutet av stycket). |
| isAfter | Boolean | Om fältet ska infogas efter eller före referensnoden. |

### Returvärde

En[`Field`](../../../aspose.words.fields/field/) objekt som representerar det infogade fältet.

## Exempel

Visar olika sätt att lägga till fält i ett stycke.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nedan följer tre sätt att infoga ett fält i ett stycke.
// 1 - Infoga ett AUTHOR-fält i ett stycke efter en av styckets underordnade noder:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Infoga ett CITAT-fält efter en av styckets underordnade noder:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Infoga ett CITAT-fält före en av styckets undernoder,
// och få den att visa ett platshållarvärde:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Det här fältet visar sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertField(*string, [Node](../../node/), bool*) {#insertfield_1}

Infogar ett fält i detta stycke.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | String | Fältkoden som ska infogas (utan klammerparenteser). |
| refNode | Node | Referensnod i detta stycke (om*refNode* är`null`, lägger sedan till i slutet av stycket). |
| isAfter | Boolean | Om fältet ska infogas efter eller före referensnoden. |

### Returvärde

En[`Field`](../../../aspose.words.fields/field/) objekt som representerar det infogade fältet.

## Exempel

Visar olika sätt att lägga till fält i ett stycke.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nedan följer tre sätt att infoga ett fält i ett stycke.
// 1 - Infoga ett AUTHOR-fält i ett stycke efter en av styckets underordnade noder:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Infoga ett CITAT-fält efter en av styckets underordnade noder:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Infoga ett CITAT-fält före en av styckets undernoder,
// och få den att visa ett platshållarvärde:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Det här fältet visar sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertField(*string, string, [Node](../../node/), bool*) {#insertfield_2}

Infogar ett fält i detta stycke.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | String | Fältkoden som ska infogas (utan klammerparenteser). |
| fieldValue | String | Fältvärdet som ska infogas. Pass`null` för fält som inte har ett värde. |
| refNode | Node | Referensnod i detta stycke (om*refNode* är`null`, lägger sedan till i slutet av stycket). |
| isAfter | Boolean | Om fältet ska infogas efter eller före referensnoden. |

### Returvärde

En[`Field`](../../../aspose.words.fields/field/) objekt som representerar det infogade fältet.

## Exempel

Visar olika sätt att lägga till fält i ett stycke.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nedan följer tre sätt att infoga ett fält i ett stycke.
// 1 - Infoga ett AUTHOR-fält i ett stycke efter en av styckets underordnade noder:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Infoga ett CITAT-fält efter en av styckets underordnade noder:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Infoga ett CITAT-fält före en av styckets undernoder,
// och få den att visa ett platshållarvärde:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Det här fältet visar sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
