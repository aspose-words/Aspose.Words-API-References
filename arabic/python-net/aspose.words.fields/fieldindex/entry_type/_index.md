---
title: FieldIndex.entry_type property
linktitle: entry_type property
articleTitle: entry_type property
second_title: Aspose.Words for Python
description: "FieldIndex.entry_type property. Gets or sets an index entry type used to build the index."
type: docs
weight: 40
url: /ar/python-net/aspose.words.fields/fieldindex/entry_type/
---

## FieldIndex.entry_type property

Gets or sets an index entry type used to build the index.


```python
@property
def entry_type(self) -> str:
    ...

@entry_type.setter
def entry_type(self, value: str):
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

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

