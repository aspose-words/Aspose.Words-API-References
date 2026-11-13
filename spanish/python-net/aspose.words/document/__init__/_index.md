---
title: Document constructor
linktitle: Document constructor
articleTitle: Document constructor
second_title: Aspose.Words for Python
description: "aspose.words.Document constructor"
type: docs
weight: 10
url: /es/python-net/aspose.words/document/__init__/
---

## Document() {#default}

Creates a blank Word document.


```python
def __init__(self):
    ...
```

### Remarks

A blank document is retrieved from resources, and by default, the resulting document looks more like created by [MsWordVersion.WORD2007](../../../aspose.words.settings/mswordversion/#WORD2007).
This blank document contains a default fonts table, minimal default styles, and latent styles.

[CompatibilityOptions.optimize_for()](../../../aspose.words.settings/compatibilityoptions/optimize_for/#mswordversion) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

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
| file_name | str | File name of the document to open. |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(UnsupportedFileFormatException)) | The document format is not recognized or not supported. |
| RuntimeError (Proxy error(FileCorruptedException)) | The document appears to be corrupted and cannot be loaded. |
| RuntimeError (Proxy error(Exception)) | There is a problem with the document and it should be reported to Aspose.Words developers. |
| RuntimeError (Proxy error(IOException)) | There is an input/output exception. |
| RuntimeError (Proxy error(IncorrectPasswordException)) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| RuntimeError (Proxy error(ArgumentException)) | The name of the file cannot be null or empty string. |

## Document(file_name, load_options) {#str_loadoptions}

Opens an existing document from a file. Allows to specify additional options such as an encryption password.


```python
def __init__(self, file_name: str, load_options: aspose.words.loading.LoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | File name of the document to open. |
| load_options | [LoadOptions](../../../aspose.words.loading/loadoptions/) | Additional options to use when loading a document. Can be ``None``. |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(UnsupportedFileFormatException)) | The document format is not recognized or not supported. |
| RuntimeError (Proxy error(FileCorruptedException)) | The document appears to be corrupted and cannot be loaded. |
| RuntimeError (Proxy error(Exception)) | There is a problem with the document and it should be reported to Aspose.Words developers. |
| RuntimeError (Proxy error(IOException)) | There is an input/output exception. |
| RuntimeError (Proxy error(IncorrectPasswordException)) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| RuntimeError (Proxy error(ArgumentException)) | The name of the file cannot be null or empty string. |

## Document(stream) {#bytesio}

Opens an existing document from a stream. Automatically detects the file format.


```python
def __init__(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | Stream where to load the document from. |

### Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(UnsupportedFileFormatException)) | The document format is not recognized or not supported. |
| RuntimeError (Proxy error(FileCorruptedException)) | The document appears to be corrupted and cannot be loaded. |
| RuntimeError (Proxy error(Exception)) | There is a problem with the document and it should be reported to Aspose.Words developers. |
| RuntimeError (Proxy error(IOException)) | There is an input/output exception. |
| RuntimeError (Proxy error(IncorrectPasswordException)) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| RuntimeError (Proxy error(ArgumentNullException)) | The stream cannot be null. |
| RuntimeError (Proxy error(NotSupportedException)) | The stream does not support reading or seeking. |
| RuntimeError (Proxy error(ObjectDisposedException)) | The stream is a disposed object. |

## Document(stream, load_options) {#bytesio_loadoptions}

Opens an existing document from a stream. Allows to specify additional options such as an encryption password.


```python
def __init__(self, stream: io.BytesIO, load_options: aspose.words.loading.LoadOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | The stream where to load the document from. |
| load_options | [LoadOptions](../../../aspose.words.loading/loadoptions/) | Additional options to use when loading a document. Can be ``None``. |

### Remarks

The document must be stored at the beginning of the stream. The stream must support random positioning.




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(UnsupportedFileFormatException)) | The document format is not recognized or not supported. |
| RuntimeError (Proxy error(FileCorruptedException)) | The document appears to be corrupted and cannot be loaded. |
| RuntimeError (Proxy error(Exception)) | There is a problem with the document and it should be reported to Aspose.Words developers. |
| RuntimeError (Proxy error(IOException)) | There is an input/output exception. |
| RuntimeError (Proxy error(IncorrectPasswordException)) | The document is encrypted and requires a password to open, but you supplied an incorrect password. |
| RuntimeError (Proxy error(ArgumentNullException)) | The stream cannot be null. |
| RuntimeError (Proxy error(NotSupportedException)) | The stream does not support reading or seeking. |
| RuntimeError (Proxy error(ObjectDisposedException)) | The stream is a disposed object. |

## Examples

Shows how to create and load documents.

```python
# Hay dos formas de crear un objeto Document usando Aspose.Words.
# 1 -  Crear un documento en blanco:
doc = aw.Document()
# Los nuevos objetos Document, por defecto, vienen con el conjunto mínimo de nodos
# necesarios para comenzar a añadir contenido como texto y formas: una Section, un Body y un Paragraph.
doc.first_section.body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
# 2 -  Cargar un documento que exista en el sistema de archivos local:
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
# Los documentos cargados tendrán contenidos a los que podemos acceder y editar.
self.assertEqual('Hello World!', doc.first_section.body.first_paragraph.get_text().strip())
# Algunas operaciones que deben ocurrir durante la carga, como usar una contraseña para descifrar un documento,
# pueden realizarse pasando un objeto LoadOptions al cargar el documento.
doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx', load_options=aw.loading.LoadOptions(password='docPassword'))
self.assertEqual('Test encrypted document.', doc.first_section.body.first_paragraph.get_text().strip())
```

Shows how to create simple document.

```python
doc = aw.Document()
# Los nuevos objetos Document, por defecto, vienen con el conjunto mínimo de nodos
# necesarios para comenzar a añadir contenido como texto y formas: una Section, un Body y un Paragraph.
section = doc.append_child(aw.Section(doc)).as_section()
body = section.append_child(aw.Body(doc)).as_body()
para = body.append_child(aw.Paragraph(doc)).as_paragraph()
para.append_child(aw.Run(doc=doc, text='Hello world!'))
```

Shows how to open a document and convert it to .PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
doc.save(file_name=ARTIFACTS_DIR + 'Document.ConvertToPdf.pdf')
```

Shows how to load a PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
doc.save(ARTIFACTS_DIR + 'PDF2Word.load_pdf.pdf')
# A continuación se presentan dos formas de cargar documentos PDF usando productos Aspose.
# 1 -  Cargar como un documento Aspose.Words:
aspose_words_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.load_pdf.pdf')
self.assertEqual('Hello world!', aspose_words_doc.get_text().strip())
```

Shows how to convert a PDF to a .docx.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.pdf')
# Cargue el documento PDF que acabamos de guardar y conviértalo a .docx.
pdf_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.pdf')
pdf_doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.docx')
```

Shows how to load an encrypted Microsoft Word document.

```python
doc = None
# Aspose.Words lanza una excepción si intentamos abrir un documento cifrado sin su contraseña.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx')
# Al cargar dicho documento, la contraseña se pasa al constructor del documento usando un objeto LoadOptions.
options = aw.loading.LoadOptions(password='docPassword')
# Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
# 1 -  Cargue el documento desde el sistema de archivos local mediante el nombre de archivo:
doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx', load_options=options)
# 2 -  Cargue el documento desde un flujo:
with system_helper.io.File.open_read(MY_DIR + 'Encrypted.docx') as stream:
    doc = aw.Document(stream=stream, load_options=options)
```

Shows how to load a document using a stream.

```python
with system_helper.io.File.open_read(MY_DIR + 'Document.docx') as stream:
    doc = aw.Document(stream=stream)
    self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', doc.get_text().strip())
```

Shows how to load a document from a URL.

```python
from io import BytesIO
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
from urllib.request import urlopen
# Cree una URL que apunte a un documento Microsoft Word.
url = 'https://filesamples.com/samples/document/docx/sample3.docx'
# Descargue el documento a un arreglo de bytes, luego cargue ese arreglo en un documento usando un flujo de memoria.
with urlopen(url) as response:
    data_bytes = response.read()
with BytesIO(data_bytes) as byte_stream:
    doc = aw.Document(byte_stream)
# En esta etapa, podemos leer y editar el contenido del documento y luego guardarlo en el sistema de archivos local.
assert doc.first_section.body.paragraphs[3].get_text().strip() == 'There are eight section headings in this document. At the beginning, "Sample Document" is a level 1 heading. ' + 'The main section headings, such as "Headings" and "Lists" are level 2 headings. ' + 'The Tables section contains two sub-headings, "Simple Table" and "Complex Table," which are both level 3 headings.'
doc.save(ARTIFACTS_DIR + 'Document.LoadFromWeb.docx')
```

Shows how to open an HTML document with images from a stream using a base URI.

```python
with system_helper.io.File.open_read(MY_DIR + 'Document.html') as stream:
    # Pase el URI de la carpeta base al cargarlo
    # para que cualquier imagen con URIs relativos en el documento HTML pueda ser encontrada.
    load_options = aw.loading.LoadOptions()
    load_options.base_uri = IMAGE_DIR
    doc = aw.Document(stream=stream, load_options=load_options)
    # Verifique que la primera forma del documento contenga una imagen válida.
    shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
    self.assertTrue(shape.is_image)
    self.assertIsNotNone(shape.image_data.image_bytes)
    self.assertAlmostEqual(32, aw.ConvertUtil.point_to_pixel(points=shape.width), delta=0.01)
    self.assertAlmostEqual(32, aw.ConvertUtil.point_to_pixel(points=shape.height), delta=0.01)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

