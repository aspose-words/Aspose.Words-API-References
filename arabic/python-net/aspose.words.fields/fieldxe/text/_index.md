---
title: FieldXE.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldXE.text property. Gets or sets the text of the entry."
type: docs
weight: 70
url: /ar/python-net/aspose.words.fields/fieldxe/text/
---

## FieldXE.text property

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

Shows how to create an INDEX field, and then use XE fields to populate it with entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أنشئ حقل INDEX سيعرض إدخالًا لكل حقل XE موجود في المستند.
# كل إدخال سيعرض قيمة خاصية Text لحقل XE على الجانب الأيسر
# والصفحة التي تحتوي على حقل XE على الجانب الأيمن.
# إذا كانت حقول XE لها نفس القيمة في خاصية "Text" الخاصة بها،
# سيقوم حقل INDEX بتجميعها في إدخال واحد.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# قم بتكوين حقل INDEX لعرض حقول XE فقط التي تقع ضمن الحدود
# لعلامة مرجعية تسمى "MainBookmark"، والتي تكون خاصية "EntryType" لها قيمة "A".
# بالنسبة لكل من حقول INDEX و XE، تستخدم خاصية "EntryType" الحرف الأول فقط من قيمتها النصية.
index.bookmark_name = 'MainBookmark'
index.entry_type = 'A'
self.assertEqual(' INDEX  \\b MainBookmark \\f A', index.get_field_code())
# في صفحة جديدة، ابدأ العلامة المرجعية باسم يطابق القيمة
# لخاصية "BookmarkName" لحقل INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MainBookmark')
# سيقوم حقل INDEX بالتقاط هذا الإدخال لأنه داخل العلامة المرجعية،
# ونوع دخله يطابق أيضًا نوع إدخال حقل INDEX.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 1'
index_entry.entry_type = 'A'
self.assertEqual(' XE  "Index entry 1" \\f A', index_entry.get_field_code())
# أدرج حقل XE لن يظهر في INDEX لأن أنواع الإدخالات لا تتطابق.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 2'
index_entry.entry_type = 'B'
# أنهِ العلامة المرجعية وأدرج حقل XE بعد ذلك.
# هو من نفس نوع حقل INDEX، لكنه لن يظهر
# لأنها خارج حدود العلامة المرجعية.
builder.end_bookmark('MainBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 3'
index_entry.entry_type = 'A'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Filtering.docx')
```

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

