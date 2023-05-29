---
title: DocumentBuilder.move_to_header_footer method
linktitle: move_to_header_footer method
articleTitle: move_to_header_footer method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_header_footer method. Moves the cursor to the beginning of a header or footer in the current section."
type: docs
weight: 540
url: /python-net/aspose.words/documentbuilder/move_to_header_footer/
---

## move_to_header_footer(header_footer_type) {#headerfootertype}

Moves the cursor to the beginning of a header or footer in the current section.


```python
def move_to_header_footer(self, header_footer_type: aspose.words.HeaderFooterType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| header_footer_type | [HeaderFooterType](../../headerfootertype/) |  |

After you moved the cursor into a header or footer, you can use the rest of [DocumentBuilder](../)
methods to modify the contents of the header or footer.

If you want to create headers and footers different for the first page, you need
to set [PageSetup.different_first_page_header_footer](../../pagesetup/different_first_page_header_footer/).

If you want to create headers and footers different for even and odd pages, you need
to set [PageSetup.odd_and_even_pages_header_footer](../../pagesetup/odd_and_even_pages_header_footer/).

Use [DocumentBuilder.move_to_section()](../move_to_section/#int) to move out of the header into the main text.




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

Shows how to insert an image, and use it as a watermark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert the image into the header so that it will be visible on every page.
image = drawing.Image.from_file(IMAGE_DIR + "Transparent background logo.png")
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
shape = builder.insert_image(image)
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True

# Place the image at the center of the page.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.left = (builder.page_setup.page_width - shape.width) // 2
shape.top = (builder.page_setup.page_height - shape.height) // 2

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_watermark.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

