---
title: FieldIndex.page_range_separator property
linktitle: page_range_separator property
articleTitle: page_range_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.page_range_separator property. Gets or sets the character sequence that is used to separate the start and end of a page range."
type: docs
weight: 130
url: /tr/python-net/aspose.words.fields/fieldindex/page_range_separator/
---

## FieldIndex.page_range_separator property

Gets or sets the character sequence that is used to separate the start and end of a page range.


```python
@property
def page_range_separator(self) -> str:
    ...

@page_range_separator.setter
def page_range_separator(self, value: str):
    ...

```

### Examples

Shows how to specify a bookmark's spanned pages as a page range for an INDEX field entry.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Belgede bulunan her XE alanı için bir giriş gösterecek bir INDEX alanı oluşturun.
# Her giriş, XE alanının Text özelliği değerini sol tarafta gösterecek,
# ve XE alanını içeren sayfanın numarasını sağ tarafta.
# INDEX girdisi, "Text" özelliğinde eşleşen değerlere sahip tüm XE alanlarını toplayacak
# her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişe.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Sayfa aralıklarını gösteren INDEX girişleri için bir ayırıcı dize belirtebiliriz
# bu, ilk sayfanın numarası ile son sayfanın numarası arasında görünecektir.
index.page_number_separator = ', on page(s) '
index.page_range_separator = ' to '
self.assertEqual(' INDEX  \\e ", on page(s) " \\g " to "', index.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'My entry'
# Bir XE alanı, PageRangeBookmarkName özelliğini kullanarak bir yer imi adlandırıyorsa,
# INDEX girişi, yer iminin kapsadığı sayfa aralığını gösterecektir
# XE alanını içeren sayfanın numarası yerine.
index_entry.page_range_bookmark_name = 'MyBookmark'
self.assertEqual(' XE  "My entry" \\r MyBookmark', index_entry.get_field_code())
self.assertEqual('MyBookmark', index_entry.page_range_bookmark_name)
# Sayfa 3'te başlayan ve sayfa 5'te sona eren bir yer imi ekleyin.
# Bu yer imine referans veren XE alanı için INDEX girişi bu sayfa aralığını gösterecektir.
# Tablomuzda, INDEX girişi "My entry, on page(s) 3 to 5" ifadesini gösterecektir.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MyBookmark')
builder.write('Start of MyBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('End of MyBookmark')
builder.end_bookmark('MyBookmark')
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.PageRangeBookmark.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

