---
title: FieldTA.page_range_bookmark_name property
linktitle: page_range_bookmark_name property
articleTitle: page_range_bookmark_name property
second_title: Aspose.Words for Python
description: "FieldTA.page_range_bookmark_name property. Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number."
type: docs
weight: 60
url: /ar/python-net/aspose.words.fields/fieldta/page_range_bookmark_name/
---

## FieldTA.page_range_bookmark_name property

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

Shows how to build and customize a table of authorities using TOA and TA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج حقل TOA، والذي سيُنشئ إدخالًا لكل حقل TA في المستند،
# مع عرض الاستشهادات الطويلة وأرقام الصفحات لكل إدخال.
field_toa = builder.insert_field(field_type=FieldType.FIELD_TOA, update_field=False).as_field_toa()
# حدد فئة الإدخال لجدولنا. سيشمل هذا TOA الآن فقط حقول TA
# التي لديها قيمة مطابقة في خاصية EntryCategory الخاصة بها.
field_toa.entry_category = '1'
# علاوة على ذلك، فئة جدول السلطات عند الفهرس 1 هي "Cases",
# والتي ستظهر كعنوان جدولنا إذا ضبطنا هذا المتغير على true.
field_toa.use_heading = True
# يمكننا تصفية حقول TA أكثر بتسمية إشارة مرجعية يجب أن تكون ضمن حدود TOA.
field_toa.bookmark_name = 'MyBookmark'
# بشكل افتراضي، يظهر تبويب بخط منقط على كامل الصفحة بين استشهاد حقل TA
# ورقم صفحته. يمكننا استبداله بأي نص نضعه في هذه الخاصية.
# إدراج حرف تبويب سيحافظ على التبويب الأصلي.
field_toa.entry_separator = ' \t p.'
# إذا كان لدينا عدة إدخالات TA تشترك في نفس الاستشهاد الطويل،
# ستظهر جميع أرقام صفحاتهم المقابلة في صف واحد.
# يمكننا استخدام هذه الخاصية لتحديد سلسلة ستفصل أرقام صفحاتهم.
field_toa.page_number_list_separator = ' & p. '
# يمكننا تعيين هذا إلى true لجعل جدولنا يعرض كلمة "passim"
# إذا كان هناك خمسة أرقام صفحات أو أكثر في صف واحد.
field_toa.use_passim = True
# يمكن لحقل TA واحد الإشارة إلى نطاق من الصفحات.
# يمكننا تحديد سلسلة هنا لتظهر بين رقم الصفحة البداية والنهاية لمثل هذه النطاقات.
field_toa.page_range_separator = ' to '
# سيتم نقل التنسيق من حقول TA إلى جدولنا.
# يمكننا تعطيل هذا عن طريق تعيين علامة RemoveEntryFormatting.
field_toa.remove_entry_formatting = True
builder.font.color = Color.green
builder.font.name = 'Arial Black'
self.assertEqual(' TOA  \\c 1 \\h \\b MyBookmark \\e " \t p." \\l " & p. " \\p \\g " to " \\f', field_toa.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# لن يظهر حقل TA هذا كإدخال في TOA لأنه خارج
# حدود العلامة المرجعية التي تحددها خاصية BookmarkName في TOA.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 1')
self.assertEqual(' TA  \\c 1 \\l "Source 1"', field_ta.get_field_code())
# حقل TA هذا داخل العلامة المرجعية،
# لكن فئة الإدخال لا تتطابق مع فئة الجدول، لذا لن يتضمن حقل TA ذلك.
builder.start_bookmark('MyBookmark')
field_ta = ExField._insert_toa_entry(builder, '2', 'Source 2')
# سيظهر هذا الإدخال في الجدول.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
# جدول TOA لا يعرض الاقتباسات المختصرة،
# لكن يمكننا استخدامها كاختصار للإشارة إلى أسماء مصادر ضخمة التي تشير إليها حقول TA متعددة.
field_ta.short_citation = 'S.3'
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\s S.3', field_ta.get_field_code())
# يمكننا تنسيق رقم الصفحة لجعله غامق/مائل باستخدام الخصائص التالية.
# سنظل نرى هذه التأثيرات إذا عيّننا جدولنا لتجاهل التنسيق.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 2')
field_ta.is_bold = True
field_ta.is_italic = True
self.assertEqual(' TA  \\c 1 \\l "Source 2" \\b \\i', field_ta.get_field_code())
# يمكننا تكوين حقول TA لجعل إدخالات TOA الخاصة بها تشير إلى نطاق من الصفحات التي تمتد عبر العلامة المرجعية.
# لاحظ أن هذا الإدخال يشير إلى نفس المصدر كما في الإدخال أعلاه لمشاركة صف واحد في جدولنا.
# سيحتوي هذا الصف على رقم صفحة الإدخال أعلاه ونطاق صفحات هذا الإدخال،
# مع قائمة صفحات الجدول وفواصل نطاق أرقام الصفحات بين أرقام الصفحات.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
field_ta.page_range_bookmark_name = 'MyMultiPageBookmark'
builder.start_bookmark('MyMultiPageBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.end_bookmark('MyMultiPageBookmark')
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\r MyMultiPageBookmark', field_ta.get_field_code())
# إذا كنا قد فعلنا ميزة "Passim" في جدولنا، فإن وجود 5 أو أكثر من إدخالات TA بنفس المصدر سيفعلها.
i = 0
while i < 5:
    ExField._insert_toa_entry(builder, '1', 'Source 4')
    i += 1
builder.end_bookmark('MyBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOA.TA.docx')
```

Shows how to build and customize a table of authorities using TOA and TA fields (InsertToaEntry).

```python
@staticmethod
def _insert_toa_entry(builder, entry_category, long_citation):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOA_ENTRY, update_field=False).as_field_ta()
    field.entry_category = entry_category
    field.long_citation = long_citation
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    return field
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldTA](../)

