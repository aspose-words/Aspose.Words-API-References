---
title: Paragraph.appendField method
linktitle: appendField method
articleTitle: appendField method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Paragraph.appendField method"
type: docs
weight: 230
url: /nodejs-net/aspose.words/paragraph/appendField/
---

## appendField(fieldType, updateField) {#fieldtype_boolean}

Appends a field to this paragraph.


```js
appendField(fieldType: Aspose.Words.Fields.FieldType, updateField: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | [FieldType](../../../aspose.words.fields/fieldtype/) | The type of the field to append. |
| updateField | boolean | Specifies whether to update the field immediately. |

### Returns

A [Field](../../field/) object that represents the appended field.


## appendField(fieldCode) {#string}

Appends a field to this paragraph.


```js
appendField(fieldCode: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | string | The field code to append (without curly braces). |

### Returns

A [Field](../../field/) object that represents the appended field.


## appendField(fieldCode, fieldValue) {#string_string}

Appends a field to this paragraph.


```js
appendField(fieldCode: string, fieldValue: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | string | The field code to append (without curly braces). |
| fieldValue | string | The field value to append. Pass ``null`` for fields that do not have a value. |

### Returns

A [Field](../../field/) object that represents the appended field.


## Examples

Shows various ways of appending fields to a paragraph.

```js
let doc = new aw.Document();
let paragraph = doc.firstSection.body.firstParagraph;

// Below are three ways of appending a field to the end of a paragraph.
// 1 -  Append a DATE field using a field type, and then update it:
paragraph.appendField(aw.Fields.FieldType.FieldDate, true);

// 2 -  Append a TIME field using a field code: 
paragraph.appendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Append a QUOTE field using a field code, and get it to display a placeholder value:
paragraph.appendField(" QUOTE \"Real value\"", "Placeholder value");

expect(doc.range.fields.at(2).result).toEqual("Placeholder value");

// This field will display its placeholder value until we update it.
doc.updateFields();

expect(doc.range.fields.at(2).result).toEqual("Real value");

doc.save(base.artifactsDir + "Paragraph.appendField.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

