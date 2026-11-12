---
title: FieldXE.page_number_replacement property
linktitle: page_number_replacement property
articleTitle: page_number_replacement property
second_title: Aspose.Words for Python
description: "FieldXE.page_number_replacement property. Gets or sets text used in place of a page number."
type: docs
weight: 50
url: /tr/python-net/aspose.words.fields/fieldxe/page_number_replacement/
---

## FieldXE.page_number_replacement property

Gets or sets text used in place of a page number.


```python
@property
def page_number_replacement(self) -> str:
    ...

@page_number_replacement.setter
def page_number_replacement(self, value: str):
    ...

```

### Examples

Shows how to define cross references in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Belgede bulunan her XE alanı için bir giriş gösterecek bir INDEX alanı oluşturun.
# Her giriş, XE alanının Text özelliği değerini sol tarafta gösterecek,
# ve XE alanını içeren sayfanın numarasını sağ tarafta.
# INDEX girdisi, "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacak
# her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişe.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Bir XE alanını, INDEX girdisinin sayfa numarası yerine bir dize göstermesi için yapılandırabiliriz.
# İlk olarak, sayfa numarasını bir dizeyle değiştiren girdiler için,
# XE alanının Text özelliği değeri ile dize arasına özel bir ayırıcı belirtin.
index.cross_reference_separator = ', see: '
self.assertEqual(' INDEX  \\k ", see: "', index.get_field_code())
# Bu alanın sayfa numarasını gösteren normal bir INDEX girdisi oluşturan bir XE alanı ekleyin,
# ve CrossReferenceSeparator değerini çağırmaz.
# Bu XE alanının girişi "Apple, 2" olarak görüntülenecek.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
self.assertEqual(' XE  Apple', index_entry.get_field_code())
# Sayfa 3'te başka bir XE alanı ekleyin ve PageNumberReplacement özelliği için bir değer ayarlayın.
# Bu değer, alanın bulunduğu sayfanın numarası yerine görünecek,
# ve INDEX alanının CrossReferenceSeparator değeri onun önünde görünecek.
# Bu XE alanının girişi "Banana, see: Tropical fruit" olarak görüntülenecek.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
index_entry.page_number_replacement = 'Tropical fruit'
self.assertEqual(' XE  Banana \\t "Tropical fruit"', index_entry.get_field_code())
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.CrossReferenceSeparator.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

