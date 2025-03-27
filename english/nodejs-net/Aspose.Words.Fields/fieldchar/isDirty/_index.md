---
title: FieldChar.isDirty property
linktitle: isDirty property
articleTitle: isDirty property
second_title: Aspose.Words for NodeJs
description: "FieldChar.isDirty property. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Fields/fieldchar/isDirty/
---

## FieldChar.isDirty property

Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications
made to the document.


```js
get isDirty(): boolean
```

### Examples

Shows how to work with a FieldStart node.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let field = builder.insertField(aw.Fields.FieldType.FieldDate, true).asFieldDate();
field.format.dateTimeFormat = "dddd, MMMM dd, yyyy";
field.update();

let fieldStart = field.start;

expect(fieldStart.fieldType).toEqual(aw.Fields.FieldType.FieldDate);
expect(fieldStart.isDirty).toEqual(false);
expect(fieldStart.isLocked).toEqual(false);

// Retrieve the facade object which represents the field in the document.
field = fieldStart.getField().asFieldDate();

expect(field.isLocked).toEqual(false);
expect(field.getFieldCode()).toEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"");

// Update the field to show the current date.
field.update();
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [FieldChar](../)

