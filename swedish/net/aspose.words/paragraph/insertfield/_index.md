---
title: InsertField
second_title: Aspose.Words för .NET API Referens
description: Infogar ett fält i detta stycke.
type: docs
weight: 270
url: /sv/net/aspose.words/paragraph/insertfield/
---
## InsertField(FieldType, bool, Node, bool) {#insertfield}

Infogar ett fält i detta stycke.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldType | FieldType | Typen av fält som ska infogas. |
| updateField | Boolean | Anger om fältet ska uppdateras omedelbart. |
| refNode | Node | Referensnod inuti det här stycket (om refNode är null, läggs det till i slutet av stycket). |
| isAfter | Boolean | Om fältet ska infogas efter eller före referensnoden. |

### Returvärde

A[`Field`](../../../aspose.words.fields/field) objekt som representerar det infogade fältet.

### Exempel

Visar olika sätt att lägga till fält i ett stycke.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nedan finns tre sätt att infoga ett fält i ett stycke.
// 1 - Infoga ett AUTHOR-fält i ett stycke efter en av styckets underordnade noder:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Infoga ett CITAT-fält efter en av styckets underordnade noder:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Infoga ett CITAT-fält före en av styckets underordnade noder,
// och få det att visa ett platshållarvärde:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field)
* enum [FieldType](../../../aspose.words.fields/fieldtype)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* namnutrymme [Aspose.Words](../../paragraph)
* hopsättning [Aspose.Words](../../../)

---

## InsertField(string, Node, bool) {#insertfield_1}

Infogar ett fält i detta stycke.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | String | Fältkoden som ska infogas (utan hängslen). |
| refNode | Node | Referensnod inuti det här stycket (om refNode är null, läggs det till i slutet av stycket). |
| isAfter | Boolean | Om fältet ska infogas efter eller före referensnoden. |

### Returvärde

A[`Field`](../../../aspose.words.fields/field) objekt som representerar det infogade fältet.

### Exempel

Visar olika sätt att lägga till fält i ett stycke.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nedan finns tre sätt att infoga ett fält i ett stycke.
// 1 - Infoga ett AUTHOR-fält i ett stycke efter en av styckets underordnade noder:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Infoga ett CITAT-fält efter en av styckets underordnade noder:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Infoga ett CITAT-fält före en av styckets underordnade noder,
// och få det att visa ett platshållarvärde:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* namnutrymme [Aspose.Words](../../paragraph)
* hopsättning [Aspose.Words](../../../)

---

## InsertField(string, string, Node, bool) {#insertfield_2}

Infogar ett fält i detta stycke.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | String | Fältkoden som ska infogas (utan hängslen). |
| fieldValue | String | Fältvärdet som ska infogas. Skicka null för fält som inte har ett värde. |
| refNode | Node | Referensnod inuti det här stycket (om refNode är null, läggs det till i slutet av stycket). |
| isAfter | Boolean | Om fältet ska infogas efter eller före referensnoden. |

### Returvärde

A[`Field`](../../../aspose.words.fields/field) objekt som representerar det infogade fältet.

### Exempel

Visar olika sätt att lägga till fält i ett stycke.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Nedan finns tre sätt att infoga ett fält i ett stycke.
// 1 - Infoga ett AUTHOR-fält i ett stycke efter en av styckets underordnade noder:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - Infoga ett CITAT-fält efter en av styckets underordnade noder:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - Infoga ett CITAT-fält före en av styckets underordnade noder,
// och få det att visa ett platshållarvärde:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// Detta fält kommer att visa sitt platshållarvärde tills vi uppdaterar det.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field)
* class [Node](../../node)
* class [Paragraph](../../paragraph)
* namnutrymme [Aspose.Words](../../paragraph)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
