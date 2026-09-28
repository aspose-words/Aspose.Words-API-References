---
title: Document constructor
linktitle: Document constructor
articleTitle: Document constructor
second_title: Aspose.Words for Python
description: "aspose.words.Document constructor"
type: docs
weight: 10
url: /fr/python-net/aspose.words/document/__init__/
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
# Il existe deux façons de créer un objet Document en utilisant Aspose.Words.
# 1 -  Créez un document vierge :
doc = aw.Document()
# Les nouveaux objets Document sont fournis par défaut avec l'ensemble minimal de nœuds
# nécessaires pour commencer à ajouter du contenu tel que du texte et des formes : une Section, un Body et un Paragraph.
doc.first_section.body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
# 2 -  Chargez un document qui existe dans le système de fichiers local :
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
# Les documents chargés auront du contenu que nous pouvons accéder et modifier.
self.assertEqual('Hello World!', doc.first_section.body.first_paragraph.get_text().strip())
# Certaines opérations qui doivent se produire lors du chargement, comme l'utilisation d'un mot de passe pour déchiffrer un document,
# peuvent être effectuées en passant un objet LoadOptions lors du chargement du document.
doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx', load_options=aw.loading.LoadOptions(password='docPassword'))
self.assertEqual('Test encrypted document.', doc.first_section.body.first_paragraph.get_text().strip())
```

Shows how to create simple document.

```python
doc = aw.Document()
# Les nouveaux objets Document sont fournis par défaut avec l'ensemble minimal de nœuds
# nécessaires pour commencer à ajouter du contenu tel que du texte et des formes : une Section, un Body et un Paragraph.
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
# Voici deux façons de charger des documents PDF en utilisant les produits Aspose.
# 1 -  Chargez en tant que document Aspose.Words :
aspose_words_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.load_pdf.pdf')
self.assertEqual('Hello world!', aspose_words_doc.get_text().strip())
```

Shows how to convert a PDF to a .docx.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.pdf')
# Chargez le document PDF que nous venons d'enregistrer, puis convertissez‑le en .docx.
pdf_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.pdf')
pdf_doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx.docx')
```

Shows how to load an encrypted Microsoft Word document.

```python
doc = None
# Aspose.Words lève une exception si nous essayons d'ouvrir un document chiffré sans son mot de passe.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx')
# Lors du chargement d'un tel document, le mot de passe est passé au constructeur du document à l'aide d'un objet LoadOptions.
options = aw.loading.LoadOptions(password='docPassword')
# Il existe deux façons de charger un document chiffré avec un objet LoadOptions.
# 1 -  Chargez le document depuis le système de fichiers local par nom de fichier :
doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx', load_options=options)
# 2 -  Chargez le document depuis un flux :
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
# Créez une URL qui pointe vers un document Microsoft Word.
url = 'https://filesamples.com/samples/document/docx/sample3.docx'
# Téléchargez le document dans un tableau d'octets, puis chargez ce tableau dans un document en utilisant un flux mémoire.
with urlopen(url) as response:
    data_bytes = response.read()
with BytesIO(data_bytes) as byte_stream:
    doc = aw.Document(byte_stream)
# À ce stade, nous pouvons lire et modifier le contenu du document, puis l'enregistrer dans le système de fichiers local.
assert doc.first_section.body.paragraphs[3].get_text().strip() == 'There are eight section headings in this document. At the beginning, "Sample Document" is a level 1 heading. ' + 'The main section headings, such as "Headings" and "Lists" are level 2 headings. ' + 'The Tables section contains two sub-headings, "Simple Table" and "Complex Table," which are both level 3 headings.'
doc.save(ARTIFACTS_DIR + 'Document.LoadFromWeb.docx')
```

Shows how to open an HTML document with images from a stream using a base URI.

```python
with system_helper.io.File.open_read(MY_DIR + 'Document.html') as stream:
    # Passez l'URI du dossier de base lors du chargement
    # afin que toutes les images avec des URI relatives dans le document HTML puissent être trouvées.
    load_options = aw.loading.LoadOptions()
    load_options.base_uri = IMAGE_DIR
    doc = aw.Document(stream=stream, load_options=load_options)
    # Vérifiez que la première forme du document contient une image valide.
    shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
    self.assertTrue(shape.is_image)
    self.assertIsNotNone(shape.image_data.image_bytes)
    self.assertAlmostEqual(32, aw.ConvertUtil.point_to_pixel(points=shape.width), delta=0.01)
    self.assertAlmostEqual(32, aw.ConvertUtil.point_to_pixel(points=shape.height), delta=0.01)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

