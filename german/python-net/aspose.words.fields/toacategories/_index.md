---
title: ToaCategories class
linktitle: ToaCategories class
articleTitle: ToaCategories class
second_title: Aspose.Words for Python
description: "aspose.words.fields.ToaCategories class. Represents a table of authorities categories"
type: docs
weight: 1320
url: /de/python-net/aspose.words.fields/toacategories/
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
# TOA-Felder können ihre Einträge nach Kategorien filtern, die in dieser Sammlung definiert sind.
toa_categories = aw.fields.ToaCategories()
doc.field_options.toa_categories = toa_categories
# Diese Sammlung von Kategorien enthält Standardwerte, die wir mit benutzerdefinierten Werten überschreiben können.
self.assertEqual('Cases', toa_categories[1])
self.assertEqual('Statutes', toa_categories[2])
toa_categories[1] = 'My Category 1'
toa_categories[2] = 'My Category 2'
# Wir können jederzeit über diese Sammlung auf die Standardwerte zugreifen.
self.assertEqual('Cases', aw.fields.ToaCategories.default_categories[1])
self.assertEqual('Statutes', aw.fields.ToaCategories.default_categories[2])
# Fügen Sie 2 TOA-Felder ein. TOA-Felder erstellen einen Eintrag für jedes TA-Feld im Dokument.
# Verwenden Sie den "\c"-Schalter, um den Index einer Kategorie aus unserer Sammlung auszuwählen.
#  Mit diesem Schalter wird ein TOA-Feld nur Einträge von TA-Feldern übernehmen, die
# auch einen "\c"-Schalter mit einem passenden Kategorienindex haben. Jedes TOA-Feld wird außerdem anzeigen
# den Namen der Kategorie, auf die sein "\c"-Schalter zeigt.
builder.insert_field(field_code='TOA \\c 1 \\h', field_value=None)
builder.insert_field(field_code='TOA \\c 2 \\h', field_value=None)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Fügen Sie TOA-Einträge über 2 Kategorien ein. Unser erstes TOA-Feld erhält einen Eintrag,
# aus dem zweiten TA-Feld, dessen "\c"-Schalter ebenfalls auf die erste Kategorie zeigt.
# Das zweite TOA-Feld wird zwei Einträge von den anderen beiden TA-Feldern haben.
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

