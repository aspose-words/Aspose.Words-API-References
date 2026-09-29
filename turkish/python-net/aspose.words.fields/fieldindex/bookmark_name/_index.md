---
title: FieldIndex.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldIndex.bookmark_name property. Gets or sets the name of the bookmark that marks the portion of the document used to build the index."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fields/fieldindex/bookmark_name/
---

## FieldIndex.bookmark_name property

Gets or sets the name of the bookmark that marks the portion of the document used to build the index.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to create an INDEX field, and then use XE fields to populate it with entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Belgede bulunan her XE alanı için bir giriş gösterecek bir INDEX alanı oluşturun.
# Her giriş, XE alanının Text property değerini sol tarafta gösterecek
# ve XE alanını içeren sayfayı sağ tarafta gösterecek.
# XE alanlarının "Text" property değerinde aynı değere sahip olması durumunda,
# INDEX alanı bunları tek bir girişte gruplayacaktır.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# INDEX alanını yalnızca sınırlar içinde olan XE alanlarını gösterecek şekilde yapılandırın
# "MainBookmark" adlı bir yer iminin içinde ve "EntryType" özelliği "A" değerine sahip olanların.
# Hem INDEX hem de XE alanları için, "EntryType" özelliği yalnızca dize değerinin ilk karakterini kullanır.
index.bookmark_name = 'MainBookmark'
index.entry_type = 'A'
self.assertEqual(' INDEX  \\b MainBookmark \\f A', index.get_field_code())
# Yeni bir sayfada, yer imini değere eşleşen bir adla başlatın
# INDEX alanının "BookmarkName" property değerine.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MainBookmark')
# INDEX alanı bu girişi alacaktır çünkü yer iminin içindedir,
# ve giriş tipi de INDEX alanının giriş tipiyle eşleşir.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 1'
index_entry.entry_type = 'A'
self.assertEqual(' XE  "Index entry 1" \\f A', index_entry.get_field_code())
# Giriş tipleri eşleşmediği için INDEX'te görünmeyecek bir XE alanı ekleyin.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 2'
index_entry.entry_type = 'B'
# Yer imini sonlandırın ve ardından bir XE alanı ekleyin.
# Bu, INDEX alanı ile aynı tipe sahiptir, ancak görünmeyecek
# çünkü yer imi sınırlarının dışındadır.
builder.end_bookmark('MainBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 3'
index_entry.entry_type = 'A'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Filtering.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

