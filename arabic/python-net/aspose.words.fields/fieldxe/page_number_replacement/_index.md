---
title: FieldXE.page_number_replacement property
linktitle: page_number_replacement property
articleTitle: page_number_replacement property
second_title: Aspose.Words for Python
description: "FieldXE.page_number_replacement property. Gets or sets text used in place of a page number."
type: docs
weight: 50
url: /ar/python-net/aspose.words.fields/fieldxe/page_number_replacement/
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
# أنشئ حقل INDEX سيعرض إدخالًا لكل حقل XE موجود في المستند.
# سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
# ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
# سيتجمع إدخال INDEX جميع حقول XE ذات القيم المطابقة في خاصية "Text"
# في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# يمكننا تكوين حقل XE لجعل إدخال INDEX يعرض سلسلة نصية بدلاً من رقم الصفحة.
# أولاً، بالنسبة للإدخالات التي تستبدل رقم الصفحة بسلسلة نصية،
# حدد فاصلًا مخصصًا بين قيمة خاصية Text لحقل XE والسلسلة.
index.cross_reference_separator = ', see: '
self.assertEqual(' INDEX  \\k ", see: "', index.get_field_code())
# أدرج حقل XE، الذي ينشئ إدخال INDEX عادي يعرض رقم صفحة هذا الحقل،
# ولا يستدعي قيمة CrossReferenceSeparator.
# سيعرض الإدخال لهذا الحقل XE "Apple, 2".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
self.assertEqual(' XE  Apple', index_entry.get_field_code())
# أدرج حقل XE آخر في الصفحة 3 وحدد قيمة لخاصية PageNumberReplacement.
# ستظهر هذه القيمة بدلاً من رقم الصفحة التي يتواجد فيها هذا الحقل،
# وسيظهر قيمة CrossReferenceSeparator لحقل INDEX أمامها.
# سيعرض الإدخال لهذا الحقل XE "Banana, see: Tropical fruit".
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

