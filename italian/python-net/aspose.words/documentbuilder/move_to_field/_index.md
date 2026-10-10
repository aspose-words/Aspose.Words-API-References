---
title: DocumentBuilder.move_to_field method
linktitle: move_to_field method
articleTitle: move_to_field method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_field method. Moves the cursor to a field in the document."
type: docs
weight: 570
url: /it/python-net/aspose.words/documentbuilder/move_to_field/
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
# Inserisci un campo usando DocumentBuilder e aggiungi un run di testo dopo di esso.
field = builder.insert_field(field_code=' AUTHOR "John Doe" ')
# Il cursore del builder è attualmente alla fine del documento.
self.assertIsNone(builder.current_node)
# Sposta il cursore sul campo specificando se posizionarlo prima o dopo il campo.
builder.move_to_field(field, move_cursor_to_after_the_field)
# Nota che il cursore è fuori dal campo in entrambi i casi.
# Ciò significa che non possiamo modificare il campo usando il builder in questo modo.
# Per modificare un campo, possiamo usare il metodo MoveTo del builder su un FieldStart di un campo
# oppure sul nodo FieldSeparator per posizionare il cursore all'interno.
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

