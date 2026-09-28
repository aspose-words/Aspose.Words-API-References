---
title: FieldToc.custom_styles property
linktitle: custom_styles property
articleTitle: custom_styles property
second_title: Aspose.Words for Python
description: "FieldToc.custom_styles property. Gets or sets a list of styles other than the built-in heading styles to include in the table of contents."
type: docs
weight: 40
url: /ar/python-net/aspose.words.fields/fieldtoc/custom_styles/
---

## FieldToc.custom_styles property

Gets or sets a list of styles other than the built-in heading styles to include in the table of contents.


```python
@property
def custom_styles(self) -> str:
    ...

@custom_styles.setter
def custom_styles(self, value: str):
    ...

```

### Examples

Shows how to insert a TOC, and populate it with entries based on heading styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
# أدرج حقل فهرس المحتويات (TOC)، والذي سيجمع جميع العناوين في جدول المحتويات.
# لكل عنوان، سيُنشئ هذا الحقل سطرًا بالنص بتنسيق ذلك العنوان إلى اليسار،
# والصفحة التي يظهر فيها العنوان إلى اليمين.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# استخدم خاصية BookmarkName لتسرد العناوين فقط
# التي تظهر ضمن حدود إشارة مرجعية باسم "MyBookmark".
field.bookmark_name = 'MyBookmark'
# النص الذي يحتوي على نمط عنوان مدمج، مثل "Heading 1"، سيُعد كعنوان.
# يمكننا تسمية أنماط إضافية لتُلتقط كعناوين بواسطة الفهرس في هذه الخاصية ومستويات الفهرس الخاصة بها.
field.custom_styles = 'Quote; 6; Intense Quote; 7'
# بشكل افتراضي، يتم فصل مستويات الأنماط/الفهرس في خاصية CustomStyles بفاصلة،
# ولكن يمكننا تعيين فاصل مخصص في هذه الخاصية.
doc.field_options.custom_toc_style_separator = ';'
# قم بتكوين الحقل لاستبعاد أي عناوين لها مستويات فهرس خارج هذا النطاق.
field.heading_level_range = '1-3'
# لن يعرض الفهرس أرقام صفحات العناوين التي مستويات فهرسها ضمن هذا النطاق.
field.page_number_omitting_level_range = '2-5'
# حدد سلسلة مخصصة تفصل كل عنوان عن رقم صفحته.
field.entry_separator = '-'
field.insert_hyperlinks = True
field.hide_in_web_layout = False
field.preserve_line_breaks = True
field.preserve_tabs = True
field.use_paragraph_outline_level = False
self.insert_new_page_with_heading(builder, 'First entry', 'Heading 1')
builder.writeln('Paragraph text.')
self.insert_new_page_with_heading(builder, 'Second entry', 'Heading 1')
self.insert_new_page_with_heading(builder, 'Third entry', 'Quote')
self.insert_new_page_with_heading(builder, 'Fourth entry', 'Intense Quote')
# سيتم حذف أرقام الصفحات لهذين العنوانين لأنهما ضمن النطاق "2-5".
self.insert_new_page_with_heading(builder, 'Fifth entry', 'Heading 2')
self.insert_new_page_with_heading(builder, 'Sixth entry', 'Heading 3')
# هذا الإدخال لا يظهر لأن "Heading 4" خارج النطاق "1-3" الذي حددناه مسبقًا.
self.insert_new_page_with_heading(builder, 'Seventh entry', 'Heading 4')
builder.end_bookmark('MyBookmark')
builder.writeln('Paragraph text.')
# هذا الإدخال لا يظهر لأنه خارج العلامة المرجعية المحددة بواسطة جدول المحتويات.
self.insert_new_page_with_heading(builder, 'Eighth entry', 'Heading 1')
self.assertEqual(' TOC  \\b MyBookmark \\t "Quote; 6; Intense Quote; 7" \\o 1-3 \\n 2-5 \\p - \\h \\u0000 \\w', field.get_field_code())
field.update_page_numbers()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.docx')
```

Shows how to insert a TOC, and populate it with entries based on heading styles (InsertNewPageWithHeading).

```python
def insert_new_page_with_heading(self, builder, caption_text, style_name):
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    original_style = builder.paragraph_format.style_name
    builder.paragraph_format.style = builder.document.styles.get_by_name(style_name)
    builder.writeln(caption_text)
    builder.paragraph_format.style = builder.document.styles.get_by_name(original_style)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

