---
title: Paragraph.insertField method
linktitle: insertField method
articleTitle: insertField method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Paragraph.insertField method"
type: docs
weight: 290
url: /nodejs-net/aspose.words/paragraph/insertField/
---

## insertField(fieldType, updateField, refNode, isAfter) {#fieldtype_boolean_node_boolean}

Inserts a field into this paragraph.


```js
insertField(fieldType: Aspose.Words.Fields.FieldType, updateField: boolean, refNode: Aspose.Words.Node, isAfter: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | [FieldType](../../../aspose.words.fields/fieldtype/) | The type of the field to insert. |
| updateField | boolean | Specifies whether to update the field immediately. |
| refNode | [Node](../../node/) | Reference node inside this paragraph (if *refNode* is``null``, then appends to the end of the paragraph). |
| isAfter | boolean | Whether to insert the field after or before reference node. |

### Returns

A [Field](../../field/) object that represents the inserted field.


## insertField(fieldCode, refNode, isAfter) {#string_node_boolean}

Inserts a field into this paragraph.


```js
insertField(fieldCode: string, refNode: Aspose.Words.Node, isAfter: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | string | The field code to insert (without curly braces). |
| refNode | [Node](../../node/) | Reference node inside this paragraph (if *refNode* is``null``, then appends to the end of the paragraph). |
| isAfter | boolean | Whether to insert the field after or before reference node. |

### Returns

A [Field](../../field/) object that represents the inserted field.


## insertField(fieldCode, fieldValue, refNode, isAfter) {#string_string_node_boolean}

Inserts a field into this paragraph.


```js
insertField(fieldCode: string, fieldValue: string, refNode: Aspose.Words.Node, isAfter: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldCode | string | The field code to insert (without curly braces). |
| fieldValue | string | The field value to insert. Pass ``null`` for fields that do not have a value. |
| refNode | [Node](../../node/) | Reference node inside this paragraph (if *refNode* is``null``, then appends to the end of the paragraph). |
| isAfter | boolean | Whether to insert the field after or before reference node. |

### Returns

A [Field](../../field/) object that represents the inserted field.


## See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

