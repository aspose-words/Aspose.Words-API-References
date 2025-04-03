---
title: FieldChar.getField method
linktitle: getField method
articleTitle: getField method
second_title: Aspose.Words for NodeJs
description: "FieldChar.getField method. Returns a field for the field char."
type: docs
weight: 40
url: /nodejs-net/aspose.words.fields/fieldchar/getField/
---

## getField() {#default}

Returns a field for the field char.


```js
getField()
```

### Remarks

A new [Field](../../../aspose.words/field/) object is created each time the method is called.



### Returns

A field for the field char.


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

