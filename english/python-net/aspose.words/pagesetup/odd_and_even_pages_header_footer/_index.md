---
title: PageSetup.odd_and_even_pages_header_footer property
linktitle: odd_and_even_pages_header_footer property
articleTitle: odd_and_even_pages_header_footer property
second_title: Aspose.Words for Python
description: "PageSetup.odd_and_even_pages_header_footer property. True if the document has different headers and footers for odd-numbered and even-numbered pages."
type: docs
weight: 280
url: /python-net/aspose.words/pagesetup/odd_and_even_pages_header_footer/
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
builder = aw.DocumentBuilder(doc)

# Specify that we want different headers and footers for first, even and odd pages.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True

# Create the headers, then add three pages to the document to display each header type.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.write("Header for the first page")
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.write("Header for even pages")
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write("Header for all other pages")

builder.move_to_section(0)
builder.writeln("Page1")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page2")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page3")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.headers_and_footers.docx")
```

Shows how to enable or disable even page headers/footers.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two types of header/footers.
# 1 -  The "Primary" header/footer, which appears on every page in the section.
# We can override the primary header/footer by a first and an even page header/footer.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln("Primary header.")

builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln("Primary footer.")

# 2 -  The "Even" header/footer, which appears on every even page of this section.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.writeln("Even page header.")

builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_EVEN)
builder.writeln("Even page footer.")

builder.move_to_section(0)
builder.writeln("Page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 2.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 3.")

# Each section has a "page_setup" object that specifies page appearance-related properties
# such as orientation, size, and borders.
# Set the "odd_and_even_pages_header_Footer" property to "True"
# to display the even page header/footer on even pages.
# Set the "odd_and_even_pages_header_Footer" property to "False"
# to display the primary header/footer on even pages.
builder.page_setup.odd_and_even_pages_header_footer = odd_and_even_pages_header_footer

doc.save(ARTIFACTS_DIR + "PageSetup.odd_and_even_pages_header_footer.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

