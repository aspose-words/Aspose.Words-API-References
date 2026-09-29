---
title: FieldIndex.use_yomi property
linktitle: use_yomi property
articleTitle: use_yomi property
second_title: Aspose.Words for Python
description: "FieldIndex.use_yomi property. Gets or sets whether to enable the use of yomi text for index entries."
type: docs
weight: 170
url: /tr/python-net/aspose.words.fields/fieldindex/use_yomi/
---

## FieldIndex.use_yomi property

Gets or sets whether to enable the use of yomi text for index entries.


```python
@property
def use_yomi(self) -> bool:
    ...

@use_yomi.setter
def use_yomi(self, value: bool):
    ...

```

### Examples

Shows how to sort INDEX field entries phonetically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Belgede bulunan her XE alanı için bir giriş gösterecek bir INDEX alanı oluşturun.
# Her giriş, XE alanının Text özelliği değerini sol tarafta gösterecek,
# ve XE alanını içeren sayfanın numarasını sağ tarafta.
# INDEX girdisi, "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacak
# her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişe.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# INDEX tablosu, girdilerini Text özelliklerinin değerlerine göre alfabetik olarak otomatik sıralar.
# INDEX tablosunu, girdileri Hiragana kullanarak fonetik olarak sıralayacak şekilde ayarlayın.
index.use_yomi = sort_entries_using_yomi
if sort_entries_using_yomi:
    self.assertEqual(' INDEX  \\y', index.get_field_code())
else:
    self.assertEqual(' INDEX ', index.get_field_code())
# INDEX alanının içindekiler tablosunda giriş olarak görünecek 4 XE alanı ekleyin.
# "Text" özelliği bir kelimenin Kanji yazımını içerebilir, telaffuzu belirsiz olabilir,
# kelimenin "Yomi" sürümü ise Hiragana kullanarak tam olarak nasıl telaffuz edildiğini yazacaktır.
# INDEX alanımızı Yomi kullanacak şekilde ayarlarsak, bu girişleri sıralayacaktır
# Yomi özelliklerinin değeriyle, Text değerleri yerine.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛子'
index_entry.yomi = 'あ'
self.assertEqual(' XE  愛子 \\y あ', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '明美'
index_entry.yomi = 'あ'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '恵美'
index_entry.yomi = 'え'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛美'
index_entry.yomi = 'え'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Yomi.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

