---
title: ToaCategories indexer
linktitle: ToaCategories indexer
articleTitle: ToaCategories indexer
second_title: Aspose.Words for Python
description: "ToaCategories indexer. Gets or sets the category heading by category number."
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/toacategories/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets or sets the category heading by category number.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to specify a set of categories for TOA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Los campos TOA pueden filtrar sus entradas por categorías definidas en esta colección.
toa_categories = aw.fields.ToaCategories()
doc.field_options.toa_categories = toa_categories
# Esta colección de categorías viene con valores predeterminados, que podemos sobrescribir con valores personalizados.
self.assertEqual('Cases', toa_categories[1])
self.assertEqual('Statutes', toa_categories[2])
toa_categories[1] = 'My Category 1'
toa_categories[2] = 'My Category 2'
# Siempre podemos acceder a los valores predeterminados a través de esta colección.
self.assertEqual('Cases', aw.fields.ToaCategories.default_categories[1])
self.assertEqual('Statutes', aw.fields.ToaCategories.default_categories[2])
# Inserte 2 campos TOA. Los campos TOA crean una entrada para cada campo TA en el documento.
# Utilice el interruptor "\c" para seleccionar el índice de una categoría de nuestra colección.
#  Con este interruptor, un campo TOA solo recogerá entradas de los campos TA que
# también tengan un interruptor "\c" con un índice de categoría coincidente. Cada campo TOA también mostrará
# el nombre de la categoría a la que apunta su interruptor "\c".
builder.insert_field(field_code='TOA \\c 1 \\h', field_value=None)
builder.insert_field(field_code='TOA \\c 2 \\h', field_value=None)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Inserte entradas TOA en 2 categorías. Nuestro primer campo TOA recibirá una entrada,
# del segundo campo TA cuyo interruptor "\c" también apunta a la primera categoría.
# El segundo campo TOA tendrá dos entradas de los otros dos campos TA.
builder.insert_field(field_code='TA \\c 2 \\l "entry 1"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field(field_code='TA \\c 1 \\l "entry 2"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field(field_code='TA \\c 2 \\l "entry 3"')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'FieldOptions.TOA.Categories.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [ToaCategories](../)

