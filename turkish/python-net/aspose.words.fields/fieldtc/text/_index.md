---
title: FieldTC.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldTC.text property. Gets or sets the text of the entry."
type: docs
weight: 40
url: /tr/python-net/aspose.words.fields/fieldtc/text/
---

## FieldTC.text property

Gets or sets the text of the entry.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to insert a TOC field, and filter which TC fields end up as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# TOC alanını ekleyin; bu alan tüm TC alanlarını bir içindekiler tablosunda derleyecektir.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Alanı yalnızca "A" tipindeki TC girişlerini ve 1 ile 3 arasında bir giriş seviyesini alacak şekilde yapılandırın.
field_toc.entry_identifier = 'A'
field_toc.entry_level_range = '1-3'
self.assertEqual(' TOC  \\f A \\l 1-3', field_toc.get_field_code())
# Bu iki giriş tabloya görünecektir.
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.insert_toc_entry(builder, 'TC field 1', 'A', '1')
self.insert_toc_entry(builder, 'TC field 2', 'A', '2')
self.assertEqual(' TC  "TC field 1" \\n \\f A \\l 1', doc.range.fields[1].get_field_code())
# Bu giriş, "A" tipinden farklı olduğu için tablodan çıkarılacaktır.
self.insert_toc_entry(builder, 'TC field 3', 'B', '1')
# Bu giriş, 1-3 aralığının dışında bir giriş seviyesine sahip olduğu için tablodan çıkarılacaktır.
self.insert_toc_entry(builder, 'TC field 4', 'A', '5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TC.docx')
```

Shows how to insert a TOC field, and filter which TC fields end up as entries (InsertTocEntry).

```python
def insert_toc_entry(self, builder, text, type_identifier, entry_level):
    field_tc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC_ENTRY, update_field=True).as_field_tc()
    field_tc.omit_page_number = True
    field_tc.text = text
    field_tc.type_identifier = type_identifier
    field_tc.entry_level = entry_level
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldTC](../)

