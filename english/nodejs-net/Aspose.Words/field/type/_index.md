---
title: Field.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for NodeJs
description: "Field.type property. Gets the Microsoft Word field type."
type: docs
weight: 100
url: /nodejs-net/aspose.words/field/type/
---

## Field.type property

Gets the Microsoft Word field type.


```js
get type(): Aspose.Words.Fields.FieldType
```

### Examples

Shows how to insert a field into a document using a field code.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let field = builder.insertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

expect(field.type).toEqual(aw.Fields.FieldType.FieldDate);
expect(field.getFieldCode()).toEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"");

// This overload of the InsertField method automatically updates inserted fields.
expect((Date.now() - Date.parse(field.result)) / 86400000).toBeLessThanOrEqual(1);
```

### See Also

* module [Aspose.Words](../../)
* class [Field](../)

