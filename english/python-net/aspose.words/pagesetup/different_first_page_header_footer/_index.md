---
title: PageSetup.different_first_page_header_footer property
linktitle: different_first_page_header_footer property
articleTitle: different_first_page_header_footer property
second_title: Aspose.Words for Python
description: "PageSetup.different_first_page_header_footer property. True if a different header or footer is used on the first page."
type: docs
weight: 110
url: /python-net/aspose.words/pagesetup/different_first_page_header_footer/
---

## PageSetup.different_first_page_header_footer property

True if a different header or footer is used on the first page.


```python
@property
def different_first_page_header_footer(self) -> bool:
    ...

@different_first_page_header_footer.setter
def different_first_page_header_footer(self, value: bool):
    ...

```

### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Specify that we want different headers and footers for first, even and odd pages.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Create the headers, then add three pages to the document to display each header type.
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

Shows how to track the order in which a text replacement operation traverses nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
first_page_section = doc.first_section
logger = self.ReplaceLog()
options = aw.replacing.FindReplaceOptions(replacing_callback=logger)
# Using a different header/footer for the first page will affect the search order.
first_page_section.page_setup.different_first_page_header_footer = different_first_page_header_footer
doc.range.replace_regex(pattern='(header|footer)', replacement='', options=options)
if different_first_page_header_footer:
    self.assertEqual('First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n', logger.text.replace('\r', ''))
else:
    self.assertEqual('Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n', logger.text.replace('\r', ''))
```

Shows how to track the order in which a text replacement operation traverses nodes (ReplaceLog).

```python
class ReplaceLog(aw.replacing.IReplacingCallback):

    @property
    def text(self):
        return str.join('', self.m_text_builder)

    def __init__(self):
        self.m_text_builder = []

    def replacing(self, args):
        self.m_text_builder.append(args.match_node.get_text() + '\n')
        return aw.replacing.ReplaceAction.SKIP
```

Shows how to enable or disable primary headers/footers.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Below are two types of header/footers.
# 1 -  The "First" header/footer, which appears on the first page of the section.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.writeln('First page header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_FIRST)
builder.writeln('First page footer.')
# 2 -  The "Primary" header/footer, which appears on every page in the section.
# We can override the primary header/footer by a first and an even page header/footer.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('Primary header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('Primary footer.')
builder.move_to_section(0)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# Each section has a "PageSetup" object that specifies page appearance-related properties
# such as orientation, size, and borders.
# Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
# Set the "DifferentFirstPageHeaderFooter" property to "false"
# to make the first page display the primary header/footer.
builder.page_setup.different_first_page_header_footer = different_first_page_header_footer
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.DifferentFirstPageHeaderFooter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

