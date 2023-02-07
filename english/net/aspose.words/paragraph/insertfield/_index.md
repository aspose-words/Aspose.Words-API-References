---
title: Paragraph.InsertField
second_title: Aspose.Words for .NET API Reference
description: Inserts a field into this paragraph in C#
type: docs
weight: 270
url: /net/aspose.words/paragraph/insertfield/
---
## InsertField(FieldType, bool, Node, bool) {#insertfield}

Inserts a field into this paragraph.

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | FieldType | The type of the field to insert. |
| updateField | Boolean | Specifies whether to update the field immediately. |
| refNode | Node | Reference node inside this paragraph (if *refNode* is `null`, then appends to the end of the paragraph). |
| isAfter | Boolean | Whether to insert the field after or before reference node. |

### Return Value

A [`Field`](../../../aspose.words.fields/field/) object that represents the inserted field.

## Examples

Shows various ways of adding fields to a paragraph.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Below are three ways of inserting a field into a paragraph.
// 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
// and get it to display a placeholder value:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// This field will display its placeholder value until we update it.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### See Also

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* namespace [Aspose.Words](../../paragraph/)
* assembly [Aspose.Words](../../../)

---

## InsertField(string, Node, bool) {#insertfield_1}

Inserts a field into this paragraph.

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | String | The field code to insert (without curly braces). |
| refNode | Node | Reference node inside this paragraph (if *refNode* is `null`, then appends to the end of the paragraph). |
| isAfter | Boolean | Whether to insert the field after or before reference node. |

### Return Value

A [`Field`](../../../aspose.words.fields/field/) object that represents the inserted field.

## Examples

Shows various ways of adding fields to a paragraph.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Below are three ways of inserting a field into a paragraph.
// 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
// and get it to display a placeholder value:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// This field will display its placeholder value until we update it.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### See Also

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* namespace [Aspose.Words](../../paragraph/)
* assembly [Aspose.Words](../../../)

---

## InsertField(string, string, Node, bool) {#insertfield_2}

Inserts a field into this paragraph.

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | String | The field code to insert (without curly braces). |
| fieldValue | String | The field value to insert. Pass `null` for fields that do not have a value. |
| refNode | Node | Reference node inside this paragraph (if *refNode* is `null`, then appends to the end of the paragraph). |
| isAfter | Boolean | Whether to insert the field after or before reference node. |

### Return Value

A [`Field`](../../../aspose.words.fields/field/) object that represents the inserted field.

## Examples

Shows various ways of adding fields to a paragraph.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Below are three ways of inserting a field into a paragraph.
// 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
// and get it to display a placeholder value:
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// This field will display its placeholder value until we update it.
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### See Also

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* namespace [Aspose.Words](../../paragraph/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
