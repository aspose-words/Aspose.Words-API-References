---
title: DocumentBuilder.moveToField method
linktitle: moveToField method
articleTitle: moveToField method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.moveToField method. Moves the cursor to a field in the document."
type: docs
weight: 570
url: /nodejs-net/aspose.words/documentbuilder/moveToField/
---

## moveToField(field, isAfter) {#field_boolean}

Moves the cursor to a field in the document.


```js
moveToField(field: Aspose.Words.Fields.Field, isAfter: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| field | [Field](../../field/) | The field to move the cursor to. |
| isAfter | boolean | When ``true``, moves the cursor to be after the field end. When ``false``, moves the cursor to be before the field start. |

### Examples

Shows how to move a document builder's node insertion point cursor to a specific field.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a field using the DocumentBuilder and add a run of text after it.
let field = builder.insertField(" AUTHOR \"John Doe\" ");

// The builder's cursor is currently at end of the document.
expect(builder.currentNode).toBe(null);

// Move the cursor to the field while specifying whether to place that cursor before or after the field.
builder.moveToField(field, moveCursorToAfterTheField);

// Note that the cursor is outside of the field in both cases.
// This means that we cannot edit the field using the builder like this.
// To edit a field, we can use the builder's MoveTo method on a field's FieldStart
// or FieldSeparator node to place the cursor inside.
if (moveCursorToAfterTheField)
{
  expect(builder.currentNode).toBe(null);
  builder.write(" Text immediately after the field.");

  expect(doc.getText().trim()).toEqual("\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.");
}
else
{
  expect(builder.currentNode).toEqual(field.start);
  builder.write("Text immediately before the field. ");

  expect(doc.getText().trim()).toEqual("Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015");
}
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

