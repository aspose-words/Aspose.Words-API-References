---
title: FieldXE.is_italic property
linktitle: is_italic property
articleTitle: is_italic property
second_title: Aspose.Words for Python
description: "FieldXE.is_italic property. Gets or sets whether to apply italic formatting to the entry's page number."
type: docs
weight: 40
url: /tr/python-net/aspose.words.fields/fieldxe/is_italic/
---

## FieldXE.is_italic property

Gets or sets whether to apply italic formatting to the entry's page number.


```python
@property
def is_italic(self) -> bool:
    ...

@is_italic.setter
def is_italic(self, value: bool):
    ...

```

### Examples

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Belgede bulunan her XE alanı için bir giriş gösterecek bir INDEX alanı oluşturun.
# Her giriş, XE alanının Text özelliği değerini sol tarafta gösterecek,
# ve XE alanını içeren sayfanın numarasını sağ tarafta.
# XE alanlarının "Text" property değerinde aynı değere sahip olması durumunda,
# INDEX alanı bunları tek bir girişte gruplayacaktır.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.language_id = '1033'
# Bu özelliğin değerini "A" olarak ayarlamak, tüm girişleri ilk harflerine göre gruplandıracaktır,
# ve bu harfi her grubun üstünde büyük harfle yerleştirecek.
index.heading = 'A'
# INDEX alanı tarafından oluşturulan tabloyu 2 sütun boyunca yayılacak şekilde ayarlayın.
index.number_of_columns = '2'
# "a-c" karakter aralığının dışındaki başlangıç harflerine sahip tüm girişlerin atlanmasını ayarlayın.
index.letter_range = 'a-c'
self.assertEqual(' INDEX  \\z 1033 \\h A \\c 2 \\p a-c', index.get_field_code())
# Bu sonraki iki XE alanı, "A" başlığının altında görünecek,
# ve ilgili metin stilleri sayfa numaralarına da uygulanacaktır.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
index_entry.is_italic = True
self.assertEqual(' XE  Apple \\i', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apricot'
index_entry.is_bold = True
self.assertEqual(' XE  Apricot \\b', index_entry.get_field_code())
# Her iki sonraki XE alanı da INDEX alanlarının içindekiler tablosunda "B" ve "C" başlıkları altında yer alacak.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cherry'
# INDEX alanları tüm girişleri alfabetik olarak sıralar, bu yüzden bu giriş diğer ikisiyle birlikte "A" altında görünecek.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Avocado'
# Bu giriş, "D" harfiyle başladığı için görünmeyecek,
# bu, INDEX alanının LetterRange özelliğinin tanımladığı "a-c" karakter aralığının dışındadır.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Durian'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Formatting.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

