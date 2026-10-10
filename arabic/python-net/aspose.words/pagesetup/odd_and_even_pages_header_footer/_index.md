---
title: PageSetup.odd_and_even_pages_header_footer property
linktitle: odd_and_even_pages_header_footer property
articleTitle: odd_and_even_pages_header_footer property
second_title: Aspose.Words for Python
description: "PageSetup.odd_and_even_pages_header_footer property. True if the document has different headers and footers for odd-numbered and even-numbered pages."
type: docs
weight: 280
url: /ar/python-net/aspose.words/pagesetup/odd_and_even_pages_header_footer/
---

## PageSetup.odd_and_even_pages_header_footer property

True if the document has different headers and footers for odd-numbered and even-numbered pages.


```python
@property
def odd_and_even_pages_header_footer(self) -> bool:
    ...

@odd_and_even_pages_header_footer.setter
def odd_and_even_pages_header_footer(self, value: bool):
    ...

```

### Remarks

Note, changing this property affects all sections in the document.


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

Shows how to enable or disable even page headers/footers.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# فيما يلي نوعان من الرؤوس/التذييلات.
# 1 -  الرأس/التذييل "Primary"، الذي يظهر في كل صفحة في القسم.
# يمكننا تجاوز الرأس/التذييل الأساسي بوجود رأس/تذييل للصفحة الأولى والصفحات الزوجية.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('Primary header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('Primary footer.')
# 2 -  الرأس/التذييل "Even"، الذي يظهر في كل صفحة زوجية من هذا القسم.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.writeln('Even page header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_EVEN)
builder.writeln('Even page footer.')
builder.move_to_section(0)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# كل قسم يحتوي على كائن "PageSetup" يحدد خصائص متعلقة بمظهر الصفحة
# مثل الاتجاه والحجم والحدود.
# قم بتعيين الخاصية "OddAndEvenPagesHeaderFooter" إلى "true"
# لعرض ترويسة/تذييل الصفحة الزوجية على الصفحات الزوجية.
# قم بتعيين الخاصية "OddAndEvenPagesHeaderFooter" إلى "false"
# لعرض الترويسة/التذييل الأساسي على الصفحات الزوجية.
builder.page_setup.odd_and_even_pages_header_footer = odd_and_even_pages_header_footer
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.OddAndEvenPagesHeaderFooter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

