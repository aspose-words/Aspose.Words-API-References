---
title: Document.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.Document.save method"
type: docs
weight: 740
url: /de/python-net/aspose.words/document/save/
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
# Laden Sie das PDF-Dokument, das wir gerade gespeichert haben, und konvertieren Sie es in .docx.
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
# Erstellen Sie ein Objekt "ImageSaveOptions", das wir an die "Save"‑Methode des Dokuments übergeben können
# um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Setzen Sie "PageSet" auf "1", um die zweite Seite auszuwählen über
# den nullbasierten Index, von dem aus das Dokument gerendert werden soll.
options.page_set = aw.saving.PageSet(page=1)
# Wenn wir das Dokument im JPEG‑Format speichern, rendert Aspose.Words nur eine Seite.
# Dieses Bild wird eine Seite enthalten, beginnend mit Seite zwei,
# die einfach die zweite Seite des Originaldokuments ist.
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.OnePage.jpg', save_options=options)
```

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Erstellen Sie ein Objekt "ImageSaveOptions", das wir an die "Save"‑Methode des Dokuments übergeben können
# um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Setzen Sie die Eigenschaft "JpegQuality" auf "10", um bei der Dokumenten‑Renderung stärkere Kompression zu verwenden.
# Dies reduziert die Dateigröße des Dokuments, aber das Bild zeigt deutlichere Kompressionsartefakte.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# Setzen Sie die Eigenschaft "JpegQuality" auf "100", um bei der Dokumenten‑Renderung schwächere Kompression zu verwenden.
# Dies wird die Qualität des Bildes verbessern, allerdings auf Kosten einer erhöhten Dateigröße.
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
# Erstellen Sie ein Objekt "ImageSaveOptions", das wir an die "save"‑Methode des Dokuments übergeben können
# um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
for i in range(doc.page_count):
    # Setzen Sie die Eigenschaft "page_set" auf die Nummer der ersten Seite, von der
    # aus der das Dokument gerendert werden soll.
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
# Laden Sie das PDF-Dokument, das wir gerade gespeichert haben, und konvertieren Sie es in .docx.
pdf_doc = aw.Document(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.pdf')
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
# Setzen Sie die Eigenschaft "password", um das gespeicherte Dokument mit einem Passwort zu verschlüsseln.
save_options.password = 'MyPassword'
pdf_doc.save(ARTIFACTS_DIR + 'PDF2Word.convert_pdf_to_docx_custom.docx', save_options)
```

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie Überschriften der Ebenen 1 bis 5 ein.
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
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Das ausgegebene PDF-Dokument enthält ein Inhaltsverzeichnis, das eine Gliederung ist und die Überschriften im Dokumentkörper auflistet.
# Ein Klick auf einen Eintrag in diesem Inhaltsverzeichnis führt uns zur Position der jeweiligen Überschrift.
# Setzen Sie die "HeadingsOutlineLevels"-Eigenschaft auf "4", um alle Überschriften, deren Ebene über 4 liegt, aus der Gliederung auszuschließen.
options.outline_options.headings_outline_levels = 4
# Wenn ein Gliederungseintrag nachfolgende Einträge einer höheren Ebene zwischen sich und dem nächsten Eintrag derselben oder einer niedrigeren Ebene hat,
# erscheint links vom Eintrag ein Pfeil. Dieser Eintrag ist der "owner" mehrerer solcher "sub-entries".
# In unserem Dokument sind die Gliederungseinträge der 5. Überschriftenebene Untereinträge des zweiten Gliederungseintrags der 4. Ebene,
# Die Einträge der 4. und 5. Überschriftsebene sind Untereinträge des zweiten Eintrags der 3. Ebene und so weiter.
# Im Inhaltsverzeichnis können wir auf den Pfeil des Eintrags "owner" klicken, um alle Untereinträge ein- bzw. auszublenden.
# Setzen Sie die Eigenschaft "ExpandedOutlineLevels" auf "2", um automatisch alle Einträge der Überschriftsebene 2 und darunter im Inhaltsverzeichnis zu erweitern
# und blenden Sie alle Einträge der Ebene 3 und höher aus, wenn wir das Dokument öffnen.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

Shows how to save a document to a stream.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
with io.BytesIO() as dst_stream:
    doc.save(stream=dst_stream, save_format=aw.SaveFormat.DOCX)
    # Überprüfen Sie, dass der Stream das Dokument enthält.
    self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', aw.Document(stream=dst_stream).get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

