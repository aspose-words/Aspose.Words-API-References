---
title: FieldIndex.page_number_separator property
linktitle: page_number_separator property
articleTitle: page_number_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.page_number_separator property. Gets or sets the character sequence that is used to separate an index entry and its page number."
type: docs
weight: 120
url: /ar/python-net/aspose.words.fields/fieldindex/page_number_separator/
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
# أنشئ حقل INDEX سيعرض إدخالًا لكل حقل XE موجود في المستند.
# سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
# ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
# سوف يجمع إدخال INDEX حقول XE ذات القيم المتطابقة في خاصية "Text"
# في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# إذا كان حقل INDEX لدينا يحتوي على إدخال لمجموعة من حقول XE،
# سيعرض هذا الإدخال رقم كل صفحة تحتوي على حقل XE ينتمي إلى هذه المجموعة.
# يمكننا تعيين فواصل مخصصة لتخصيص مظهر أرقام الصفحات هذه.
index.page_number_separator = ', on page(s) '
index.page_number_list_separator = ' & '
self.assertEqual(' INDEX  \\e ", on page(s) " \\l " & "', index.get_field_code())
self.assertTrue(index.has_page_number_separator)
# بعد إدراج حقول XE هذه، سيعرض حقل INDEX "First entry, on page(s) 2 & 3 & 4".
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

