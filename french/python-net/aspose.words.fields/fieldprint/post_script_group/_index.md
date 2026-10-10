---
title: FieldPrint.post_script_group property
linktitle: post_script_group property
articleTitle: post_script_group property
second_title: Aspose.Words for Python
description: "FieldPrint.post_script_group property. Gets or sets the drawing rectangle that the PostScript instructions operate on."
type: docs
weight: 20
url: /fr/python-net/aspose.words.fields/fieldprint/post_script_group/
---

## FieldPrint.post_script_group property

Gets or sets the drawing rectangle that the PostScript instructions operate on.


```python
@property
def post_script_group(self) -> str:
    ...

@post_script_group.setter
def post_script_group(self, value: str):
    ...

```

### Examples

Shows to insert a PRINT field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('My paragraph')
# Le champ PRINT peut envoyer des instructions à l'imprimante.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_PRINT, update_field=True).as_field_print()
# Définissez la zone sur laquelle l'imprimante exécutera les instructions.
# Dans ce cas, ce sera le paragraphe qui contient notre champ PRINT.
field.post_script_group = 'para'
# Lorsque nous utilisons une imprimante qui prend en charge PostScript pour imprimer notre document,
# cette commande rendra toute la zone que nous avons spécifiée dans "field.PostScriptGroup" blanche.
field.printer_instructions = 'erasepage'
self.assertEqual(' PRINT  erasepage \\p para', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.PRINT.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldPrint](../)

