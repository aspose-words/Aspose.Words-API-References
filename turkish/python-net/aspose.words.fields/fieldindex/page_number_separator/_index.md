---
title: FieldIndex.page_number_separator property
linktitle: page_number_separator property
articleTitle: page_number_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.page_number_separator property. Gets or sets the character sequence that is used to separate an index entry and its page number."
type: docs
weight: 120
url: /tr/python-net/aspose.words.fields/fieldindex/page_number_separator/
---

## FieldIndex.page_number_separator property

Gets or sets the character sequence that is used to separate an index entry and its page number.


```python
@property
def page_number_separator(self) -> str:
    ...

@page_number_separator.setter
def page_number_separator(self, value: str):
    ...

```

### Examples

Shows how to edit the page number separator in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Belgede bulunan her XE alanı için bir giriş gösterecek bir INDEX alanı oluşturun.
# Her giriş, XE alanının Text özelliği değerini sol tarafta gösterecek,
# ve XE alanını içeren sayfanın numarasını sağ tarafta.
# INDEX girişi, "Text" özelliğinde eşleşen değerlere sahip XE alanlarını gruplayacaktır
# her XE alanı için ayrı bir giriş oluşturmak yerine tek bir girişe.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# INDEX alanımızın bir grup XE alanı için bir girişi varsa,
# bu giriş, bu gruba ait bir XE alanı içeren her sayfanın numarasını gösterecektir.
# Bu sayfa numaralarının görünümünü özelleştirmek için özel ayırıcılar ayarlayabiliriz.
index.page_number_separator = ', on page(s) '
index.page_number_list_separator = ' & '
self.assertEqual(' INDEX  \\e ", on page(s) " \\l " & "', index.get_field_code())
self.assertTrue(index.has_page_number_separator)
# Bu XE alanlarını ekledikten sonra, INDEX alanı "İlk giriş, sayfa(lar) 2 & 3 & 4" şeklinde görüntülenecek.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
self.assertEqual(' XE  "First entry"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.PageNumberList.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

