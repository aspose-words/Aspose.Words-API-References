---
title: DocumentBuilder.move_to_field method
linktitle: move_to_field method
articleTitle: move_to_field method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_field method. Moves the cursor to a field in the document."
type: docs
weight: 570
url: /fr/python-net/aspose.words/documentbuilder/move_to_field/
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
# Insérez un champ à l'aide du DocumentBuilder et ajoutez un texte après celui-ci.
field = builder.insert_field(field_code=' AUTHOR "John Doe" ')
# Le curseur du builder se trouve actuellement à la fin du document.
self.assertIsNone(builder.current_node)
# Déplacez le curseur vers le champ en précisant s'il faut placer ce curseur avant ou après le champ.
builder.move_to_field(field, move_cursor_to_after_the_field)
# Notez que le curseur se trouve à l'extérieur du champ dans les deux cas.
# Cela signifie que nous ne pouvons pas modifier le champ en utilisant le builder de cette façon.
# Pour modifier un champ, nous pouvons utiliser la méthode MoveTo du builder sur le FieldStart d'un champ
# ou le nœud FieldSeparator pour placer le curseur à l'intérieur.
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

