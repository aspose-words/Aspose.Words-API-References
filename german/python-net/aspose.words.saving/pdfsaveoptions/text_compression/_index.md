---
title: PdfSaveOptions.text_compression property
linktitle: text_compression property
articleTitle: text_compression property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.text_compression property. Specifies compression type to be used for all textual content in the document."
type: docs
weight: 330
url: /de/python-net/aspose.words.saving/pdfsaveoptions/text_compression/
---

## PdfSaveOptions.text_compression property

Specifies compression type to be used for all textual content in the document.


```python
@property
def text_compression(self) -> aspose.words.saving.PdfTextCompression:
    ...

@text_compression.setter
def text_compression(self, value: aspose.words.saving.PdfTextCompression):
    ...

```

### Remarks

Default is [PdfTextCompression.FLATE](../../pdftextcompression/#FLATE).

Significantly increases output size when saving a document without compression.




### Examples

Shows how to apply text compression when saving a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 100:
    builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    i += 1
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Setzen Sie die "TextCompression"-Eigenschaft auf "PdfTextCompression.None", um keine
# Kompression auf Text anzuwenden, wenn wir das Dokument als PDF speichern.
# Setzen Sie die "TextCompression"-Eigenschaft auf "PdfTextCompression.Flate", um ZIP-Kompression
# auf Text anzuwenden, wenn wir das Dokument als PDF speichern. Je größer das Dokument, desto größer ist die Auswirkung.
options.text_compression = pdf_text_compression
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TextCompression.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

