---
title: Document.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.Document.save method"
type: docs
weight: 670
url: /python-net/aspose.words/document/save/
---

## save(file_name) {#str}

Saves the document to a file. Automatically determines the save format from the extension.


```python
def save(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

### Returns

Additional information that you can optionally use.


## save(file_name, save_format) {#str_saveformat}

Saves the document to a file in the specified format.


```python
def save(self, file_name: str, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| save_format | [SaveFormat](../../saveformat/) |  |

### Returns

Additional information that you can optionally use.


## save(file_name, save_options) {#str_saveoptions}

Saves the document to a file using the specified save options.


```python
def save(self, file_name: str, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) |  |

### Returns

Additional information that you can optionally use.


## save(stream, save_format) {#bytesio_saveformat}

Saves the document to a stream using the specified format.


```python
def save(self, stream: BytesIO, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |
| save_format | [SaveFormat](../../saveformat/) |  |

### Returns

Additional information that you can optionally use.


## save(stream, save_options) {#bytesio_saveoptions}

Saves the document to a stream using the specified save options.


```python
def save(self, stream: BytesIO, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) |  |

### Returns

Additional information that you can optionally use.


## Examples

Shows how to open a document and convert it to .PDF.

```python
doc = aw.Document(MY_DIR + "Document.docx")

doc.save(ARTIFACTS_DIR + "Document.convert_to_pdf.pdf")
```

Shows how to convert a PDF to a .docx.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Hello world!")

doc.save(ARTIFACTS_DIR + "PDF2Word.convert_pdf_to_docx.pdf")

# Load the PDF document that we just saved, and convert it to .docx.
pdf_doc = aw.Document(ARTIFACTS_DIR + "PDF2Word.convert_pdf_to_docx.pdf")

pdf_doc.save(ARTIFACTS_DIR + "PDF2Word.convert_pdf_to_docx.docx")
```

Shows how to convert from DOCX to HTML format.

```python
doc = aw.Document(MY_DIR + "Document.docx")

doc.save(ARTIFACTS_DIR + "Document.convert_to_html.html", aw.SaveFormat.HTML)
```

Shows how to improve the quality of a rendered document with SaveOptions.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")
builder = aw.DocumentBuilder(doc)

builder.font.size = 60
builder.writeln("Some text.")

options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)

doc.save(ARTIFACTS_DIR + "Document.image_save_options.default.jpg", options)

options.use_anti_aliasing = True
options.use_high_quality_rendering = True

doc.save(ARTIFACTS_DIR + "Document.image_save_options.high_quality.jpg", options)
```

Shows how to render one page from a document to a JPEG image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 2.")
builder.insert_image(IMAGE_DIR + "Logo.jpg")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 3.")

# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)

# Set the "page_set" to "1" to select the second page via
# the zero-based index to start rendering the document from.
options.page_set = aw.saving.PageSet(1)

# When we save the document to the JPEG format, Aspose.Words only renders one page.
# This image will contain one page starting from page two,
# which will just be the second page of the original document.
doc.save(ARTIFACTS_DIR + "ImageSaveOptions.one_page.jpg", options)
```

Shows how to render every page of a document to a separate TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 2.")
builder.insert_image(IMAGE_DIR + "Logo.jpg")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 3.")

# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)

for i in range(doc.page_count):

    # Set the "page_set" property to the number of the first page from
    # which to start rendering the document from.
    options.page_set = aw.saving.PageSet(i)

    doc.save(ARTIFACTS_DIR + f"ImageSaveOptions.page_by_page.{i + 1}.tiff", options)
```

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.insert_image(IMAGE_DIR + "Logo.jpg")

# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)

# Set the "jpeg_quality" property to "10" to use stronger compression when rendering the document.
# This will reduce the file size of the document, but the image will display more prominent compression artifacts.
image_options.jpeg_quality = 10

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_compression.jpg", image_options)

self.assertGreater(20000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_compression.jpg"))

# Set the "jpeg_quality" property to "100" to use weaker compression when rending the document.
# This will improve the quality of the image at the cost of an increased file size.
image_options.jpeg_quality = 100

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_quality.jpg", image_options)

self.assertLess(40000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_quality.jpg"))
```

Shows how to convert a PDF to a .docx and customize the saving process with a SaveOptions object.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")

doc.save(ARTIFACTS_DIR + "PDF2Word.convert_pdf_to_docx_custom.pdf")

# Load the PDF document that we just saved, and convert it to .docx.
pdf_doc = aw.Document(ARTIFACTS_DIR + "PDF2Word.convert_pdf_to_docx_custom.pdf")

save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)

# Set the "password" property to encrypt the saved document with a password.
save_options.password = "MyPassword"

pdf_doc.save(ARTIFACTS_DIR + "PDF2Word.convert_pdf_to_docx_custom.docx", save_options)
```

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert headings of levels 1 to 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1

self.assertTrue(builder.paragraph_format.is_heading)

builder.writeln("Heading 1")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2

builder.writeln("Heading 1.1")
builder.writeln("Heading 1.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3

builder.writeln("Heading 1.2.1")
builder.writeln("Heading 1.2.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4

builder.writeln("Heading 1.2.2.1")
builder.writeln("Heading 1.2.2.2")

builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5

builder.writeln("Heading 1.2.2.2.1")
builder.writeln("Heading 1.2.2.2.2")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
# Clicking on an entry in this outline will take us to the location of its respective heading.
# Set the "headings_outline_levels" property to "4" to exclude all headings whose levels are above 4 from the outline.
options.outline_options.headings_outline_levels = 4

# If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
# an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
# In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
# the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
# In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
# Set the "expanded_outline_levels" property to "2" to automatically expand all heading level 2 and lower outline entries
# and collapse all level and 3 and higher entries when we open the document.
options.outline_options.expanded_outline_levels = 2

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.expanded_outline_levels.pdf", options)
```

Shows how to save a document to an image via stream, and then read the image from that stream.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Times New Roman"
builder.font.size = 24
builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")

builder.insert_image(IMAGE_DIR + "Logo.jpg")

with io.BytesIO() as stream:
    doc.save(stream, aw.SaveFormat.BMP)

    stream.seek(0, os.SEEK_SET)

    # Read the stream back into an image.
    with drawing.Image.from_stream(stream) as image:
        self.assertEqual(drawing.imaging.ImageFormat.bmp, image.raw_format)
        self.assertEqual(816, image.width)
        self.assertEqual(1056, image.height)
```

Shows how to save a document to a stream.

```python
doc = aw.Document(MY_DIR + "Document.docx")

with io.BytesIO() as dst_stream:
    doc.save(dst_stream, aw.SaveFormat.DOCX)

    # Verify that the stream contains the document.
    self.assertEqual("Hello World!\r\rHello Word!\r\r\rHello World!", aw.Document(dst_stream).get_text().strip())
```

Shows how to convert only some of the pages in a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 2.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 3.")

with open(ARTIFACTS_DIR + "PdfSaveOptions.one_page.pdf", "wb") as stream:

    # Create a "PdfSaveOptions" object that we can pass to the document's "save" method
    # to modify how that method converts the document to .PDF.
    options = aw.saving.PdfSaveOptions()

    # Set the "page_index" to "1" to render a portion of the document starting from the second page.
    options.page_set = aw.saving.PageSet(1)

    # This document will contain one page starting from page two, which will only contain the second page.
    doc.save(stream, options)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

