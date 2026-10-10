---
title: Document.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.Document.save method"
type: docs
weight: 740
url: /it/python-net/aspose.words/document/save/
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
# Carica il documento PDF che abbiamo appena salvato e convertilo in .docx.
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
# Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo rende il documento in un'immagine.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Imposta "PageSet" a "1" per selezionare la seconda pagina tramite
# l'indice basato su zero da cui iniziare a rendere il documento.
options.page_set = aw.saving.PageSet(page=1)
# Quando salviamo il documento nel formato JPEG, Aspose.Words rende solo una pagina.
# Questa immagine conterrà una pagina a partire dalla pagina due,
# che sarà semplicemente la seconda pagina del documento originale.
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.OnePage.jpg', save_options=options)
```

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo rende il documento in un'immagine.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Imposta la proprietà "JpegQuality" a "10" per usare una compressione più forte durante il rendering del documento.
# Ciò ridurrà la dimensione del file del documento, ma l'immagine mostrerà artefatti di compressione più evidenti.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# Imposta la proprietà "JpegQuality" a "100" per usare una compressione più debole durante il rendering del documento.
# Questo migliorerà la qualità dell'immagine a costo di un aumento delle dimensioni del file.
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
# Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "save" del documento
# per modificare il modo in cui quel metodo rende il documento in un'immagine.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
for i in range(doc.page_count):
    # Imposta la proprietà "page_set" al numero della prima pagina da
    # cui iniziare a rendere il documento.
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
# Carica il documento PDF che abbiamo appena salvato e convertilo in .docx.
pdf_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.pdf')
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
# Imposta la proprietà "password" per crittografare il documento salvato con una password.
save_options.password = 'MyPassword'
pdf_doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.docx', save_options)
```

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci intestazioni di livello da 1 a 5.
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
options = aw.saving.PdfSaveOptions()
# Il documento PDF di output conterrà un sommario, che è una tabella dei contenuti che elenca le intestazioni nel corpo del documento.
# Fare clic su una voce di questa struttura ci porterà alla posizione della relativa intestazione.
# Imposta la proprietà "HeadingsOutlineLevels" su "4" per escludere tutte le intestazioni i cui livelli sono superiori a 4 dal sommario.
options.outline_options.headings_outline_levels = 4
# Se una voce del sommario ha voci successive di livello superiore tra sé e la voce successiva dello stesso livello o inferiore,
# apparirà una freccia a sinistra della voce. Questa voce è il "owner" di diverse "sub-entries".
# Nel nostro documento, le voci del sommario dal livello di intestazione 5 sono sub-entries della seconda voce del sommario di livello 4
# le voci di livello 4 e 5 sono sotto‑voci della seconda voce di livello 3, e così via.
# Nell'indice, possiamo fare clic sulla freccia della voce "owner" per comprimere/espandere tutte le sue sotto‑voci.
# Imposta la proprietà "ExpandedOutlineLevels" a "2" per espandere automaticamente tutte le voci di indice di livello 2 e inferiori
# e comprimi tutte le voci di livello 3 e superiori quando apriamo il documento.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

Shows how to save a document to a stream.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
with io.BytesIO() as dst_stream:
    doc.save(stream=dst_stream, save_format=aw.SaveFormat.DOCX)
    # Verifica che lo stream contenga il documento.
    self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', aw.Document(stream=dst_stream).get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

