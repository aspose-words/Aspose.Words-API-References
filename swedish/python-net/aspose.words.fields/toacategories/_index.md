---
title: ToaCategories class
linktitle: ToaCategories class
articleTitle: ToaCategories class
second_title: Aspose.Words for Python
description: "aspose.words.fields.ToaCategories class. Represents a table of authorities categories"
type: docs
weight: 1320
url: /sv/python-net/aspose.words.fields/toacategories/
---

## ToaCategories class

Represents a table of authorities categories.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [ToaCategories()](./__init__/#default) | The default constructor. |

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets the category heading by category number. |

### Properties

| Name | Description |
| --- | --- |
| [default_categories](./default_categories/) | Gets the default table of authorities categories. |

### Examples

Shows how to specify a set of categories for TOA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# TOA-fält kan filtrera sina poster efter kategorier som definieras i denna samling.
toa_categories = aw.fields.ToaCategories()
doc.field_options.toa_categories = toa_categories
# Denna samling av kategorier levereras med standardvärden, som vi kan skriva över med anpassade värden.
self.assertEqual('Cases', toa_categories[1])
self.assertEqual('Statutes', toa_categories[2])
toa_categories[1] = 'My Category 1'
toa_categories[2] = 'My Category 2'
# Vi kan alltid komma åt standardvärdena via den här samlingen.
self.assertEqual('Cases', aw.fields.ToaCategories.default_categories[1])
self.assertEqual('Statutes', aw.fields.ToaCategories.default_categories[2])
# Infoga 2 TOA-fält. TOA-fält skapar en post för varje TA-fält i dokumentet.
# Använd \"\\c\"-växeln för att välja indexet för en kategori från vår samling.
#  Med den här växeln kommer ett TOA-fält endast att hämta poster från TA-fält som
# också har en \"\\c\"-växel med ett matchande kategoriindex. Varje TOA-fält kommer också att visa
# namnet på den kategori som dess \"\\c\"-växel pekar på.
builder.insert_field(field_code='TOA \\c 1 \\h', field_value=None)
builder.insert_field(field_code='TOA \\c 2 \\h', field_value=None)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Infoga TOA-poster över 2 kategorier. Vårt första TOA-fält kommer att få en post,
# från det andra TA-fältet vars \"\\c\"-växel också pekar på den första kategorin.
# Det andra TOA-fältet kommer att ha två poster från de andra två TA-fälten.
builder.insert_field(field_code='TA \\c 2 \\l "entry 1"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field(field_code='TA \\c 1 \\l "entry 2"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field(field_code='TA \\c 2 \\l "entry 3"')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'FieldOptions.TOA.Categories.docx')
```

### See Also

* module [aspose.words.fields](../)

