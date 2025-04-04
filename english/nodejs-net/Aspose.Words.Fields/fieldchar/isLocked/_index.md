---
title: FieldChar.isLocked property
linktitle: isLocked property
articleTitle: isLocked property
second_title: Aspose.Words for Node.js
description: "FieldChar.isLocked property. Gets or sets whether the parent field is locked (should not recalculate its result)."
type: docs
weight: 30
url: /nodejs-net/aspose.words.fields/fieldchar/isLocked/
---

## FieldChar.isLocked property

Gets or sets whether the parent field is locked (should not recalculate its result).


```js
get isLocked(): boolean
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

