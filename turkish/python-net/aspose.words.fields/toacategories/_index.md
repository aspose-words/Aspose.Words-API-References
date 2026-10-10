---
title: ToaCategories class
linktitle: ToaCategories class
articleTitle: ToaCategories class
second_title: Aspose.Words for Python
description: "aspose.words.fields.ToaCategories class. Represents a table of authorities categories"
type: docs
weight: 1320
url: /tr/python-net/aspose.words.fields/toacategories/
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
# TOA alanları, bu koleksiyonda tanımlanan kategorilere göre girdilerini filtreleyebilir.
toa_categories = aw.fields.ToaCategories()
doc.field_options.toa_categories = toa_categories
# Bu kategori koleksiyonu varsayılan değerlerle gelir; bunları özel değerlerle üzerine yazabiliriz.
self.assertEqual('Cases', toa_categories[1])
self.assertEqual('Statutes', toa_categories[2])
toa_categories[1] = 'My Category 1'
toa_categories[2] = 'My Category 2'
# Bu koleksiyon aracılığıyla her zaman varsayılan değerlere erişebiliriz.
self.assertEqual('Cases', aw.fields.ToaCategories.default_categories[1])
self.assertEqual('Statutes', aw.fields.ToaCategories.default_categories[2])
# 2 TOA alanı ekleyin. TOA alanları, belgede her bir TA alanı için bir giriş oluşturur.
# "\c" anahtarını kullanarak koleksiyonumuzdan bir kategorinin dizinini seçin.
#  Bu anahtar ile, bir TOA alanı yalnızca şu TA alanlarından girişleri alır ki
# aynı zamanda eşleşen bir kategori diziniyle "\c" anahtarına sahiptir. Her TOA alanı ayrıca görüntüler
# "\c" anahtarının işaret ettiği kategorinin adını.
builder.insert_field(field_code='TOA \\c 1 \\h', field_value=None)
builder.insert_field(field_code='TOA \\c 2 \\h', field_value=None)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 2 kategori boyunca TOA girişleri ekleyin. İlk TOA alanımız bir giriş alacak,
# "\c" anahtarı da ilk kategoriye işaret eden ikinci TA alanından.
# İkinci TOA alanı diğer iki TA alanından iki giriş alacak.
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

