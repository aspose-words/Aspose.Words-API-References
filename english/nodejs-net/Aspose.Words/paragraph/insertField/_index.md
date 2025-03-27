---
title: Paragraph.insertField method
linktitle: insertField method
articleTitle: insertField method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Paragraph.insertField method"
type: docs
weight: 290
url: /nodejs-net/Aspose.Words/paragraph/insertField/
---

## insertField(fieldType, updateField, refNode, isAfter) {#fieldtype_boolean_node_boolean}

Inserts a field into this paragraph.


```js
insertField(fieldType: Aspose.Words.Fields.FieldTypeupdateField: booleanrefNode: Aspose.Words.NodeisAfter: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | [FieldType](../../../Aspose.Words.Fields/fieldtype/) | The type of the field to insert. |
| updateField | boolean | Specifies whether to update the field immediately. |
| refNode | [Node](../../node/) | Reference node inside this paragraph (if *refNode* is``None``, then appends to the end of the paragraph). |
| isAfter | boolean | Whether to insert the field after or before reference node. |

### Returns

A [Field](../../field/) object that represents the inserted field.


## insertField(fieldCode, refNode, isAfter) {#string_node_boolean}

Inserts a field into this paragraph.


```js
insertField(fieldCode: stringrefNode: Aspose.Words.NodeisAfter: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | string | The field code to insert (without curly braces). |
| refNode | [Node](../../node/) | Reference node inside this paragraph (if *refNode* is``None``, then appends to the end of the paragraph). |
| isAfter | boolean | Whether to insert the field after or before reference node. |

### Returns

A [Field](../../field/) object that represents the inserted field.


## insertField(fieldCode, fieldValue, refNode, isAfter) {#string_string_node_boolean}

Inserts a field into this paragraph.


```js
insertField(fieldCode: stringfieldValue: stringrefNode: Aspose.Words.NodeisAfter: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | string | The field code to insert (without curly braces). |
| fieldValue | string | The field value to insert. Pass ``None`` for fields that do not have a value. |
| refNode | [Node](../../node/) | Reference node inside this paragraph (if *refNode* is``None``, then appends to the end of the paragraph). |
| isAfter | boolean | Whether to insert the field after or before reference node. |

### Returns

A [Field](../../field/) object that represents the inserted field.


## Examples

Shows various ways of adding fields to a paragraph.

```js
let doc = new aw.Document();
let para = doc.firstSection.body.firstParagraph;

// Below are three ways of inserting a field into a paragraph.
// 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
let run = new aw.Run(doc);
run.text = "This run was written by ";
para.appendChild(run);

doc.builtInDocumentProperties.author = "John Doe";
para.insertField(aw.Fields.FieldType.FieldAuthor, true, run, true);

// 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
run = new aw.Run(doc);
run.text = ".";
para.appendChild(run);

let field = para.insertField(" QUOTE \" Real value\" ", run, true);

// 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
// and get it to display a placeholder value:
para.insertField(" QUOTE \" Real value.\"", " Placeholder value.", field.start, false);

expect(doc.range.fields.at(1).result).toEqual(" Placeholder value.");

// This field will display its placeholder value until we update it.
doc.updateFields();

expect(doc.range.fields.at(1).result).toEqual(" Real value.");

doc.save(base.artifactsDir + "Paragraph.insertField.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

