---
title: OutlineOptions.create_outlines_for_headings_in_tables property
linktitle: create_outlines_for_headings_in_tables property
articleTitle: create_outlines_for_headings_in_tables property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_outlines_for_headings_in_tables property. Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables."
type: docs
weight: 40
url: /ar/python-net/aspose.words.saving/outlineoptions/create_outlines_for_headings_in_tables/
---

## OutlineOptions.create_outlines_for_headings_in_tables property

Specifies whether or not to create outlines for headings (paragraphs formatted with the Heading styles) inside tables.


```python
@property
def create_outlines_for_headings_in_tables(self) -> bool:
    ...

@create_outlines_for_headings_in_tables.setter
def create_outlines_for_headings_in_tables(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.




### Examples

Shows how to create PDF document outline entries for headings inside tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# إنشاء جدول بثلاث صفوف. الصف الأول،
# الذي سننسق نصه بنمط عنوان، سيعمل كعنوان للعمود.
builder.start_table()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.write('Customers')
builder.end_row()
builder.insert_cell()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.write('John Doe')
builder.end_row()
builder.insert_cell()
builder.write('Jane Doe')
builder.end_table()
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# سيحتوي مستند PDF الناتج على مخطط، وهو جدول محتويات يسرد العناوين في جسم المستند.
# النقر على مدخل في هذا المخطط سيأخذنا إلى موقع العنوان المقابل له.
# عيّن خاصية \"HeadingsOutlineLevels\" إلى \"1\" للحصول على المخطط
# لتسجيل العناوين فقط ذات مستويات لا تتجاوز 1.
pdf_save_options.outline_options.headings_outline_levels = 1
# عيّن خاصية \"CreateOutlinesForHeadingsInTables\" إلى \"false\" لاستبعاد جميع العناوين داخل الجداول،
# مثل الجدول الذي أنشأناه أعلاه من المخطط.
# عيّن خاصية \"CreateOutlinesForHeadingsInTables\" إلى \"true\" لتضمين جميع العناوين داخل الجداول
# في المخطط، بشرط أن يكون مستوى العنوان لا يتجاوز قيمة خاصية \"HeadingsOutlineLevels\".
pdf_save_options.outline_options.create_outlines_for_headings_in_tables = create_outlines_for_headings_in_tables
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TableHeadingOutlines.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

