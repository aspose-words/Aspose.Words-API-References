---
title: DocumentBuilder.move_to_field method
linktitle: move_to_field method
articleTitle: move_to_field method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_field method. Moves the cursor to a field in the document."
type: docs
weight: 570
url: /de/python-net/aspose.words/documentbuilder/move_to_field/
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
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie ein Feld mit dem DocumentBuilder ein und fügen Sie danach einen Textlauf hinzu.
field = builder.insert_field(field_code=' AUTHOR "John Doe" ')
# Der Cursor des Builders befindet sich derzeit am Ende des Dokuments.
self.assertIsNone(builder.current_node)
# Bewegen Sie den Cursor zum Feld und geben Sie dabei an, ob der Cursor vor oder nach dem Feld platziert werden soll.
builder.move_to_field(field, move_cursor_to_after_the_field)
# Beachten Sie, dass der Cursor in beiden Fällen außerhalb des Feldes liegt.
# Das bedeutet, dass wir das Feld nicht auf diese Weise mit dem Builder bearbeiten können.
# Um ein Feld zu bearbeiten, können wir die MoveTo-Methode des Builders an einem FieldStart eines Feldes verwenden
# oder am FieldSeparator-Knoten, um den Cursor hinein zu setzen.
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

