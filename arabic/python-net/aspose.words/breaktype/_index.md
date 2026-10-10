---
title: BreakType enumeration
linktitle: BreakType enumeration
articleTitle: BreakType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.BreakType enumeration. Specifies type of a break inside a document."
type: docs
weight: 120
url: /ar/python-net/aspose.words/breaktype/
---

## BreakType enumeration

Specifies type of a break inside a document.


### Members

| Name | Description |
| --- | --- |
| PARAGRAPH_BREAK | Break between paragraphs. |
| PAGE_BREAK | Explicit page break. |
| COLUMN_BREAK | Explicit column break. |
| SECTION_BREAK_CONTINUOUS | Specifies start of new section on the same page as the previous section. |
| SECTION_BREAK_NEW_COLUMN | Specifies start of new section in the new column. |
| SECTION_BREAK_NEW_PAGE | Specifies start of new section on a new page. |
| SECTION_BREAK_EVEN_PAGE | Specifies start of new section on a new even page. |
| SECTION_BREAK_ODD_PAGE | Specifies start of new section on a odd page. |
| LINE_BREAK | Explicit line break. |

### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# حدد أننا نريد رؤوس وتذييلات مختلفة للصفحات الأولى، والصفحات الزوجية والفردية.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# أنشئ الرؤوس، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع من الرؤوس.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.write('Header for the first page')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.write('Header for even pages')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('Header for all other pages')
builder.move_to_section(0)
builder.writeln('Page1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page3')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.HeadersAndFooters.docx')
```

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج جدول محتويات للصفحة الأولى من المستند.
# قم بتكوين الجدول لالتقاط الفقرات ذات العناوين من المستوى 1 إلى 3.
# أيضًا، اضبط عناصره لتكون روابط تشعبية ستأخذنا
# إلى موقع العنوان عند النقر بزر الفأرة الأيسر في Microsoft Word.
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# املأ جدول المحتويات بإضافة فقرات باستخدام أنماط العناوين.
# كل عنوان من هذا النوع بمستوى بين 1 و 3 سيُنشئ مدخلاً في الجدول.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 2')
builder.writeln('Heading 3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 3.1.1')
builder.writeln('Heading 3.1.2')
builder.writeln('Heading 3.1.3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 3.1.3.1')
builder.writeln('Heading 3.1.3.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.2')
builder.writeln('Heading 3.3')
# جدول المحتويات هو حقل من نوع يحتاج إلى تحديث لإظهار نتيجة محدثة.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# عدّل خصائص إعداد الصفحة للقسم الحالي للمنشئ وأضف نصًا.
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln('This is the first section, which landscape oriented with vertically centered text.')
# إذا بدأنا قسمًا جديدًا باستخدام مُنشئ المستند،
# سوف يرث خصائص إعداد الصفحة الحالية للمنشئ.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)
# يمكننا إرجاع خصائص إعداد صفحته إلى القيم الافتراضية باستخدام طريقة "ClearFormatting".
builder.page_setup.clear_formatting()
self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)
builder.writeln('This is the second section, which is in default Letter paper size, portrait orientation and top alignment.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ClearFormatting.docx')
```

### See Also

* module [aspose.words](../)

