---
title: DocumentBuilder.move_to_field method
linktitle: move_to_field method
articleTitle: move_to_field method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_field method. Moves the cursor to a field in the document."
type: docs
weight: 560
url: /python-net/aspose.words/documentbuilder/move_to_field/
---

## move_to_field(field, is_after) {#field_bool}

Moves the cursor to a field in the document.


```python
def move_to_field(self, field: aspose.words.fields.Field, is_after: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field | [Field](../../../aspose.words.fields/field/) | The field to move the cursor to. |
| is_after | bool | When ``True``, moves the cursor to be after the field end. When ``False``, moves the cursor to be before the field start. |

### Examples

Shows how to move a document builder's node insertion point cursor to a specific field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a field using the DocumentBuilder and add a run of text after it.
field = builder.insert_field(' AUTHOR "John Doe" ')
# The builder's cursor is currently at end of the document.
self.assertIsNone(builder.current_node)
# Move the cursor to the field while specifying whether to place that cursor before or after the field.
builder.move_to_field(field, move_cursor_to_after_the_field)
# Note that the cursor is outside of the field in both cases.
# This means that we cannot edit the field using the builder like this.
# To edit a field, we can use the builder's "move_to" method on a field's FieldStart
# or FieldSeparator node to place the cursor inside.
if move_cursor_to_after_the_field:
    self.assertIsNone(builder.current_node)
    builder.write(' Text immediately after the field.')
    self.assertEqual('\x13 AUTHOR "John Doe" \x14John Doe\x15 Text immediately after the field.', doc.get_text().strip())
else:
    self.assertEqual(field.start, builder.current_node)
    builder.write('Text immediately before the field. ')
    self.assertEqual('Text immediately before the field. \x13 AUTHOR "John Doe" \x14John Doe\x15', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

