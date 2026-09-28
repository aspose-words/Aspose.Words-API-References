---
title: FieldXE.page_range_bookmark_name property
linktitle: page_range_bookmark_name property
articleTitle: page_range_bookmark_name property
second_title: Aspose.Words for Python
description: "FieldXE.page_range_bookmark_name property. Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number."
type: docs
weight: 60
url: /ar/python-net/aspose.words.fields/fieldxe/page_range_bookmark_name/
---

## FieldXE.page_range_bookmark_name property

Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number.


```python
@property
def page_range_bookmark_name(self) -> str:
    ...

@page_range_bookmark_name.setter
def page_range_bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to specify a bookmark's spanned pages as a page range for an INDEX field entry.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أنشئ حقل INDEX سيعرض إدخالًا لكل حقل XE موجود في المستند.
# سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
# ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
# سيتجمع إدخال INDEX جميع حقول XE ذات القيم المطابقة في خاصية "Text"
# في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# بالنسبة لإدخالات INDEX التي تعرض نطاقات الصفحات، يمكننا تحديد سلسلة فاصل
# ستظهر بين رقم الصفحة الأولى ورقم الأخيرة.
index.page_number_separator = ', on page(s) '
index.page_range_separator = ' to '
self.assertEqual(' INDEX  \\e ", on page(s) " \\g " to "', index.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'My entry'
# إذا كان حقل XE يحدد إشارة مرجعية باستخدام خاصية PageRangeBookmarkName،
# سوف يظهر إدخال INDEX نطاق الصفحات التي تغطيها الإشارة المرجعية
# بدلاً من رقم الصفحة التي تحتوي على حقل XE.
index_entry.page_range_bookmark_name = 'MyBookmark'
self.assertEqual(' XE  "My entry" \\r MyBookmark', index_entry.get_field_code())
self.assertEqual('MyBookmark', index_entry.page_range_bookmark_name)
# أدرج إشارة مرجعية تبدأ من الصفحة 3 وتنتهي في الصفحة 5.
# سيوضح إدخال INDEX لحقل XE الذي يشير إلى هذه الإشارة المرجعية نطاق الصفحات هذا.
# في جدولنا، سيعرض إدخال INDEX "My entry, on page(s) 3 to 5".
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
* class [FieldXE](../)

