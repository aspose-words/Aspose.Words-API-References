---
title: Paragraph.AppendField
linktitle: AppendField
articleTitle: AppendField
second_title: Aspose.Words for .NET
description: Enhance your document with the Paragraph AppendField method, seamlessly adding custom fields to paragraphs for improved organization and clarity.
type: docs
weight: 260
url: /net/aspose.words/paragraph/appendfield/
---
## AppendField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#appendfield}

Appends a field to this paragraph.

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | FieldType | The type of the field to append. |
| updateField | Boolean | Specifies whether to update the field immediately. |

### Return Value

A [`Field`](../../../aspose.words.fields/field/) object that represents the appended field.

## Examples

Shows various ways of appending fields to a paragraph.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Below are three ways of appending a field to the end of a paragraph.
// 1 -  Append a DATE field using a field type, and then update it:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 -  Append a TIME field using a field code: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Append a QUOTE field using a field code, and get it to display a placeholder value:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.That(doc.Range.Fields[2].Result, Is.EqualTo("Placeholder value"));

// This field will display its placeholder value until we update it.
doc.UpdateFields();

Assert.That(doc.Range.Fields[2].Result, Is.EqualTo("Real value"));

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### See Also

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## AppendField(*string*) {#appendfield_1}

Appends a field to this paragraph.

```csharp
public Field AppendField(string fieldCode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | String | The field code to append (without curly braces). |

### Return Value

A [`Field`](../../../aspose.words.fields/field/) object that represents the appended field.

## Examples

Shows various ways of appending fields to a paragraph.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Below are three ways of appending a field to the end of a paragraph.
// 1 -  Append a DATE field using a field type, and then update it:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 -  Append a TIME field using a field code: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Append a QUOTE field using a field code, and get it to display a placeholder value:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.That(doc.Range.Fields[2].Result, Is.EqualTo("Placeholder value"));

// This field will display its placeholder value until we update it.
doc.UpdateFields();

Assert.That(doc.Range.Fields[2].Result, Is.EqualTo("Real value"));

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### See Also

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## AppendField(*string, string*) {#appendfield_2}

Appends a field to this paragraph.

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | String | The field code to append (without curly braces). |
| fieldValue | String | The field value to append. Pass `null` for fields that do not have a value. |

### Return Value

A [`Field`](../../../aspose.words.fields/field/) object that represents the appended field.

## Examples

Shows various ways of appending fields to a paragraph.

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// Below are three ways of appending a field to the end of a paragraph.
// 1 -  Append a DATE field using a field type, and then update it:
paragraph.AppendField(FieldType.FieldDate, true);

// 2 -  Append a TIME field using a field code: 
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Append a QUOTE field using a field code, and get it to display a placeholder value:
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.That(doc.Range.Fields[2].Result, Is.EqualTo("Placeholder value"));

// This field will display its placeholder value until we update it.
doc.UpdateFields();

Assert.That(doc.Range.Fields[2].Result, Is.EqualTo("Real value"));

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### See Also

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
