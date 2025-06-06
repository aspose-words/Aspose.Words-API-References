﻿---
title: Document.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.Document.save method"
type: docs
weight: 720
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
| file_name | str | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |

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
| file_name | str | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| save_format | [SaveFormat](../../saveformat/) | The format in which to save the document. |

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
| file_name | str | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | Specifies the options that control how the document is saved. Can be ``None``. |

### Returns

Additional information that you can optionally use.


## save(stream, save_format) {#bytesio_saveformat}

Saves the document to a stream using the specified format.


```python
def save(self, stream: io.BytesIO, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Stream where to save the document. |
| save_format | [SaveFormat](../../saveformat/) | The format in which to save the document. |

### Returns

Additional information that you can optionally use.


## save(stream, save_options) {#bytesio_saveoptions}

Saves the document to a stream using the specified save options.


```python
def save(self, stream: io.BytesIO, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Stream where to save the document. |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | Specifies the options that control how the document is saved. Can be ``None``. If this is ``None``, the document will be saved in the binary DOC format. |

### Returns

Additional information that you can optionally use.


## Examples

Shows how to open a document and convert it to .PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Document.ConvertToPdf.pdf')
```

Shows how to convert a PDF to a .docx.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.pdf')
# Load the PDF document that we just saved, and convert it to .docx.
pdf_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.pdf')
pdf_doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.docx')
```

Shows how to convert from DOCX to HTML format.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Document.ConvertToHtml.html', save_format=aw.SaveFormat.HTML)
```

Shows how to improve the quality of a rendered document with SaveOptions.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.font.size = 60
builder.writeln('Some text.')
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
doc.save(file_name=ARTIFACTS_DIR + 'Document.ImageSaveOptions.Default.jpg', save_options=options)
options.use_anti_aliasing = True
options.use_high_quality_rendering = True
doc.save(file_name=ARTIFACTS_DIR + 'Document.ImageSaveOptions.HighQuality.jpg', save_options=options)
```

Shows how to render one page from a document to a JPEG image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
# to modify the way in which that method renders the document into an image.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Set the "PageSet" to "1" to select the second page via
# the zero-based index to start rendering the document from.
options.page_set = aw.saving.PageSet(page=1)
# When we save the document to the JPEG format, Aspose.Words only renders one page.
# This image will contain one page starting from page two,
# which will just be the second page of the original document.
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.OnePage.jpg', save_options=options)
```

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
# to modify the way in which that method renders the document into an image.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
# This will reduce the file size of the document, but the image will display more prominent compression artifacts.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
# This will improve the quality of the image at the cost of an increased file size.
image_options.jpeg_quality = 100
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighQuality.jpg', save_options=image_options)
```

Shows how to render every page of a document to a separate TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_image(IMAGE_DIR + 'Logo.jpg')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
for i in range(doc.page_count):
    # Set the "page_set" property to the number of the first page from
    # which to start rendering the document from.
    options.page_set = aw.saving.PageSet(i)
    options.vertical_resolution = 600
    options.horizontal_resolution = 600
    options.image_size = aspose.pydrawing.Size(2325, 5325)
    doc.save(ARTIFACTS_DIR + f'ImageSaveOptions.page_by_page.{i + 1}.tiff', options)
```

Shows how to convert a PDF to a .docx and customize the saving process with a SaveOptions object.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Hello world!')
doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.pdf')
# Load the PDF document that we just saved, and convert it to .docx.
pdf_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.pdf')
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
# Set the "password" property to encrypt the saved document with a password.
save_options.password = 'MyPassword'
pdf_doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.docx', save_options)
```

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert headings of levels 1 to 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
# Clicking on an entry in this outline will take us to the location of its respective heading.
# Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
options.outline_options.headings_outline_levels = 4
# If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
# an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
# In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
# the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
# In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
# Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
# and collapse all level and 3 and higher entries when we open the document.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

Shows how to save a document to a stream.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
with io.BytesIO() as dst_stream:
    doc.save(stream=dst_stream, save_format=aw.SaveFormat.DOCX)
    # Verify that the stream contains the document.
    self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', aw.Document(stream=dst_stream).get_text().strip())
```

Shows how to save a document to an image via stream, and then read the image from that stream.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.font.name = 'Times New Roman'
builder.font.size = 24
builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
builder.insert_image(IMAGE_DIR + 'Logo.jpg')
with io.BytesIO() as stream:
    doc.save(stream, aw.SaveFormat.BMP)
    stream.seek(0, os.SEEK_SET)
    # Read the stream back into an image.
    with aspose.pydrawing.Image.from_stream(stream) as image:
        self.assertEqual(aspose.pydrawing.imaging.ImageFormat.bmp, image.raw_format)
        self.assertEqual(816, image.width)
        self.assertEqual(1056, image.height)
```

Shows how to convert only some of the pages in a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
with open(ARTIFACTS_DIR + 'PdfSaveOptions.one_page.pdf', 'wb') as stream:
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

