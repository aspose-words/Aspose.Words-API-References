---
title: FieldXE.is_bold property
linktitle: is_bold property
articleTitle: is_bold property
second_title: Aspose.Words for Python
description: "FieldXE.is_bold property. Gets or sets whether to apply bold formatting to the entry's page number."
type: docs
weight: 30
url: /ar/python-net/aspose.words.fields/fieldxe/is_bold/
---

## FieldXE.is_bold property

Gets or sets whether to apply bold formatting to the entry's page number.


```python
@property
def is_bold(self) -> bool:
    ...

@is_bold.setter
def is_bold(self, value: bool):
    ...

```

### Examples

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أنشئ حقل INDEX سيعرض إدخالًا لكل حقل XE موجود في المستند.
# سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
# ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
# إذا كانت حقول XE لها نفس القيمة في خاصية "Text" الخاصة بها،
# سيقوم حقل INDEX بتجميعها في إدخال واحد.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.language_id = '1033'
# ضبط قيمة هذه الخاصية إلى "A" سيجعل جميع الإدخالات تُجمع حسب الحرف الأول لها،
# ويضع ذلك الحرف بحروف كبيرة فوق كل مجموعة.
index.heading = 'A'
# اجعل الجدول الذي أنشأه حقل INDEX يمتد على عمودين.
index.number_of_columns = '2'
# اجعل أي إدخالات تبدأ بحروف خارج النطاق "a-c" تُحذف.
index.letter_range = 'a-c'
self.assertEqual(' INDEX  \\z 1033 \\h A \\c 2 \\p a-c', index.get_field_code())
# سوف تظهر الحقلين التاليين من نوع XE تحت العنوان "A"،
# مع تطبيق تنسيقات النص الخاصة بهما أيضًا على أرقام الصفحات.
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
# كلا الحقلين التاليين من نوع XE سيكونان تحت عناوين "B" و "C" في جدول محتويات حقول INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cherry'
# حقول INDEX تقوم بترتيب جميع الإدخالات أبجديًا، لذا سيظهر هذا الإدخال تحت "A" مع الآخرين.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Avocado'
# هذا الإدخال لن يظهر لأنه يبدأ بالحرف "D"،
# وهو خارج النطاق "a-c" الذي تحدده خاصية LetterRange لحقل INDEX.
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

