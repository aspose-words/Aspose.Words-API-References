---
title: FieldXE.yomi property
linktitle: yomi property
articleTitle: yomi property
second_title: Aspose.Words for Python
description: "FieldXE.yomi property. Gets or sets the yomi (first phonetic character for sorting indexes) for the index entry"
type: docs
weight: 80
url: /python-net/aspose.words.fields/fieldxe/yomi/
---

## FieldXE.yomi property

Gets or sets the yomi (first phonetic character for sorting indexes) for the index entry


```python
@property
def yomi(self) -> str:
    ...

@yomi.setter
def yomi(self, value: str):
    ...

```

### Examples

Shows how to sort INDEX field entries phonetically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Create an INDEX field which will display an entry for each XE field found in the document.
# Each entry will display the XE field's Text property value on the left side,
# and the number of the page that contains the XE field on the right.
# The INDEX entry will collect all XE fields with matching values in the "Text" property
# into one entry as opposed to making an entry for each XE field.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# The INDEX table automatically sorts its entries by the values of their Text properties in alphabetic order.
# Set the INDEX table to sort entries phonetically using Hiragana instead.
index.use_yomi = sort_entries_using_yomi
if sort_entries_using_yomi:
    self.assertEqual(' INDEX  \\y', index.get_field_code())
else:
    self.assertEqual(' INDEX ', index.get_field_code())
# Insert 4 XE fields, which would show up as entries in the INDEX field's table of contents.
# The "Text" property may contain a word's spelling in Kanji, whose pronunciation may be ambiguous,
# while the "Yomi" version of the word will spell exactly how it is pronounced using Hiragana.
# If we set our INDEX field to use Yomi, it will sort these entries
# by the value of their Yomi properties, instead of their Text values.
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
* class [FieldXE](../)

