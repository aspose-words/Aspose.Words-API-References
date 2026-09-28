---
title: FieldIndex.cross_reference_separator property
linktitle: cross_reference_separator property
articleTitle: cross_reference_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.cross_reference_separator property. Gets or sets the character sequence that is used to separate cross references and other entries."
type: docs
weight: 30
url: /ar/python-net/aspose.words.fields/fieldindex/cross_reference_separator/
---

## FieldIndex.cross_reference_separator property

Gets or sets the character sequence that is used to separate cross references and other entries.


```python
@property
def cross_reference_separator(self) -> str:
    ...

@cross_reference_separator.setter
def cross_reference_separator(self, value: str):
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
* class [FieldIndex](../)

