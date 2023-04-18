---
title: Document constructor
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.Document constructor"
type: docs
weight: 10
url: /python-net/aspose.words/document/__init__/
---

## Document() {#default}

Creates a blank Word document.


```python
def __init__(self):
    ...
```

The document paper size is Letter by default. If you want to change page setup, use
[Section.page_setup](../../section/page_setup/).

After creation, you can use [DocumentBuilder](../../documentbuilder/) to add document content easily.




## Document(file_name) {#str}

Opens an existing document from a file. Automatically detects the file format.


```python
def __init__(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| System.Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| System.IO.IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| System.ArgumentException | The name of the file cannot be null or empty string. |

## Document(file_name, load_options) {#str_loadoptions}

Opens an existing document from a file. Allows to specify additional options such as an encryption password.


```python
def __init__(self, file_name: str, load_options: aspose.words.loading.LoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| load_options | [LoadOptions](../../../aspose.words.loading/loadoptions/) |  |

### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| System.Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| System.IO.IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| System.ArgumentException | The name of the file cannot be null or empty string. |

## Document(stream) {#bytesio}

Opens an existing document from a stream. Automatically detects the file format.


```python
def __init__(self, stream: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |

The document must be stored at the beginning of the stream. The stream must support random positioning.




### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| System.Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| System.IO.IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| System.ArgumentNullException | The stream cannot be null. |
| System.NotSupportedException | The stream does not support reading or seeking. |
| System.ObjectDisposedException | The stream is a disposed object. |

## Document(stream, load_options) {#bytesio_loadoptions}

Opens an existing document from a stream. Allows to specify additional options such as an encryption password.


```python
def __init__(self, stream: BytesIO, load_options: aspose.words.loading.LoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |
| load_options | [LoadOptions](../../../aspose.words.loading/loadoptions/) |  |

The document must be stored at the beginning of the stream. The stream must support random positioning.




### Exceptions

| exception | condition |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | The document format is not recognized or not supported. |
| [FileCorruptedException](../../filecorruptedexception/) | The document appears to be corrupted and cannot be loaded. |
| System.Exception | There is a problem with the document and it should be reported to Aspose.Words developers. |
| System.IO.IOException | There is an input/output exception. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| System.ArgumentNullException | The stream cannot be null. |
| System.NotSupportedException | The stream does not support reading or seeking. |
| System.ObjectDisposedException | The stream is a disposed object. |

## Examples

Shows how to create and load documents.

```python
# There are two ways of creating a Document object using Aspose.Words.
# 1 -  Create a blank document:
doc = aw.Document()

# New Document objects by default come with the minimal set of nodes
# required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc.first_section.body.first_paragraph.append_child(aw.Run(doc, "Hello world!"))

# 2 -  Load a document that exists in the local file system:
doc = aw.Document(MY_DIR + "Document.docx")

# Loaded documents will have contents that we can access and edit.
self.assertEqual("Hello World!", doc.first_section.body.first_paragraph.get_text().strip())

# Some operations that need to occur during loading, such as using a password to decrypt a document,
# can be done by passing a LoadOptions object when loading the document.
doc = aw.Document(MY_DIR + "Encrypted.docx", aw.loading.LoadOptions("docPassword"))

self.assertEqual("Test encrypted document.", doc.first_section.body.first_paragraph.get_text().strip())
```

Shows how to format a run of text using its font property.

```python
doc = aw.Document()
run = aw.Run(doc, "Hello world!")

font = run.font
font.name = "Courier New"
font.size = 36
font.highlight_color = drawing.Color.yellow

doc.first_section.body.first_paragraph.append_child(run)
doc.save(ARTIFACTS_DIR + "Font.create_formatted_run.docx")
```

Shows how to open a document and convert it to .PDF.

```python
doc = aw.Document(MY_DIR + "Document.docx")

doc.save(ARTIFACTS_DIR + "Document.convert_to_pdf.pdf")
```

Shows how to load a PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Hello world!")

doc.save(ARTIFACTS_DIR + "PDF2Word.load_pdf.pdf")

# Below are two ways of loading PDF documents using Aspose products.
# 1 -  Load as an Aspose.Words document:
aspose_words_doc = aw.Document(ARTIFACTS_DIR + "PDF2Word.load_pdf.pdf")

self.assertEqual("Hello world!", aspose_words_doc.get_text().strip())

# 2 -  Load as an Aspose.Pdf document:
aspose_pdf_doc = aw.Document(ARTIFACTS_DIR + "PDF2Word.load_pdf.pdf")

text_fragment_absorber = aspose.pdf.text.TextFragmentAbsorber()
aspose_pdf_doc.pages.accept(text_fragment_absorber)

self.assertEqual("Hello world!", text_fragment_absorber.text.strip())
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

Shows how to load an encrypted Microsoft Word document.

```python
# Aspose.Words throw an exception if we try to open an encrypted document without its password.
with self.assertRaises(Exception):
    doc = aw.Document(MY_DIR + "Encrypted.docx")

# When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
options = aw.loading.LoadOptions("docPassword")

# There are two ways of loading an encrypted document with a LoadOptions object.
# 1 -  Load the document from the local file system by filename:
doc = aw.Document(MY_DIR + "Encrypted.docx", options)

# 2 -  Load the document from a stream:
with open(MY_DIR + "Encrypted.docx", "rb") as stream:
    doc = aw.Document(stream, options)
```

Shows how to load a document using a stream.

```python
with open(MY_DIR + "Document.docx", "rb") as stream:
    doc = aw.Document(stream)

    self.assertEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.get_text().strip())
```

Shows how to load a document from a URL.

```python
# Create a URL that points to a Microsoft Word document.
url = "https://omextemplates.content.office.net/support/templates/en-us/tf16402488.dotx"

# Download the document into a byte array, then load that array into a document using a memory stream.
data_bytes = urlopen(url).read()

with io.BytesIO(data_bytes) as byte_stream:
    doc = aw.Document(byte_stream)

    # At this stage, we can read and edit the document's contents and then save it to the local file system.
    self.assertEqual(
        "Use this section to highlight your relevant passions, activities, and how you like to give back. " +
        "It’s good to include Leadership and volunteer experiences here. " +
        "Or show off important extras like publications, certifications, languages and more.",
        doc.first_section.body.paragraphs[4].get_text().strip())

    doc.save(ARTIFACTS_DIR + "Document.load_from_web.docx")
```

Shows how to open an HTML document with images from a stream using a base URI.

```python
with open(MY_DIR + "Document.html", "rb") as stream:
    # Pass the URI of the base folder while loading it
    # so that any images with relative URIs in the HTML document can be found.
    load_options = aw.loading.LoadOptions()
    load_options.base_uri = IMAGE_DIR

    doc = aw.Document(stream, load_options)

    # Verify that the first shape of the document contains a valid image.
    shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

    self.assertTrue(shape.is_image)
    self.assertIsNotNone(shape.image_data.image_bytes)
    self.assertAlmostEqual(32.0, aw.ConvertUtil.point_to_pixel(shape.width), delta=0.01)
    self.assertAlmostEqual(32.0, aw.ConvertUtil.point_to_pixel(shape.height), delta=0.01)
```

Shows how save a web page as a .docx file.

```python
url = "https://www.aspose.com/"

with io.BytesIO(urlopen(url).read()) as stream:
    # The URL is used again as a "base_uri" to ensure that any relative image paths are retrieved correctly.
    options = aw.loading.LoadOptions(aw.LoadFormat.HTML, "", url)

    # Load the HTML document from stream and pass the LoadOptions object.
    doc = aw.Document(stream, options)

    # At this stage, we can read and edit the document's contents and then save it to the local file system.
    self.assertEqual("HYPERLINK \"https://products.aspose.com/words/family/\" \\o \"Aspose.Words\"",

    doc.save(ARTIFACTS_DIR + "Document.insert_html_from_web_page.docx")
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

