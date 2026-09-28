---
title: DocumentBuilder.insert_break method
linktitle: insert_break method
articleTitle: insert_break method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_break method. Inserts a break of the specified type into the document."
type: docs
weight: 260
url: /ar/python-net/aspose.words/documentbuilder/insert_break/
---

## insert_break(break_type) {#breaktype}

Inserts a break of the specified type into the document.


```python
def insert_break(self, break_type: aspose.words.BreakType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| break_type | [BreakType](../../breaktype/) | Specifies the type of the break to insert. |

### Remarks

Use this method to insert paragraph, page, column, section or line break into the document.


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

* module [aspose.words](../../)
* class [DocumentBuilder](../)

