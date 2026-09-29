---
title: ToaCategories.default_categories property
linktitle: default_categories property
articleTitle: default_categories property
second_title: Aspose.Words for Python
description: "ToaCategories.default_categories property. Gets the default table of authorities categories."
type: docs
weight: 30
url: /it/python-net/aspose.words.fields/toacategories/default_categories/
---

## ToaCategories.default_categories property

Gets the default table of authorities categories.


```python
@property
def default_categories(self) -> aspose.words.fields.ToaCategories:
    ...

```

### Remarks

Use the [FieldOptions.toa_categories](../../fieldoptions/toa_categories/) property to specify table of authorities categories for a single document.



### Examples

Shows how to specify a set of categories for TOA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# I campi TOA possono filtrare le loro voci per categorie definite in questa raccolta.
toa_categories = aw.fields.ToaCategories()
doc.field_options.toa_categories = toa_categories
# Questa raccolta di categorie include valori predefiniti, che possiamo sovrascrivere con valori personalizzati.
self.assertEqual('Cases', toa_categories[1])
self.assertEqual('Statutes', toa_categories[2])
toa_categories[1] = 'My Category 1'
toa_categories[2] = 'My Category 2'
# Possiamo sempre accedere ai valori predefiniti tramite questa collezione.
self.assertEqual('Cases', aw.fields.ToaCategories.default_categories[1])
self.assertEqual('Statutes', aw.fields.ToaCategories.default_categories[2])
# Inserisci 2 campi TOA. I campi TOA creano una voce per ogni campo TA nel documento.
# Usa l'opzione "\c" per selezionare l'indice di una categoria dalla nostra collezione.
#  Con questa opzione, un campo TOA prenderà solo le voci dai campi TA che
# hanno anche un'opzione "\c" con un indice di categoria corrispondente. Ogni campo TOA mostrerà anche
# il nome della categoria a cui punta la sua opzione "\c".
builder.insert_field(field_code='TOA \\c 1 \\h', field_value=None)
builder.insert_field(field_code='TOA \\c 2 \\h', field_value=None)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Inserisci voci TOA in 2 categorie. Il nostro primo campo TOA riceverà una voce,
# dal secondo campo TA il cui "\c" punta anche alla prima categoria.
# Il secondo campo TOA avrà due voci dagli altri due campi TA.
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

