---
title: FieldOptions.toa_categories property
linktitle: toa_categories property
articleTitle: toa_categories property
second_title: Aspose.Words for Python
description: "FieldOptions.toa_categories property. Gets or sets the table of authorities categories."
type: docs
weight: 190
url: /es/python-net/aspose.words.fields/fieldoptions/toa_categories/
---

## FieldOptions.toa_categories property

Gets or sets the table of authorities categories.


```python
@property
def toa_categories(self) -> aspose.words.fields.ToaCategories:
    ...

@toa_categories.setter
def toa_categories(self, value: aspose.words.fields.ToaCategories):
    ...

```

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
* class [FieldOptions](../)

