---
title: PdfTextCompression enumeration
linktitle: PdfTextCompression enumeration
articleTitle: PdfTextCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfTextCompression enumeration. Specifies a type of compression applied to all content in the PDF file except images."
type: docs
weight: 760
url: /it/python-net/aspose.words.saving/pdftextcompression/
---

## PdfTextCompression enumeration

Specifies a type of compression applied to all content in the PDF file except images.


### Members

| Name | Description |
| --- | --- |
| NONE | No compression. |
| FLATE | Flate (ZIP) compression. |

### Examples

Shows how to apply text compression when saving a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 100:
    builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    i += 1
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
options = aw.saving.PdfSaveOptions()
# Imposta la proprietà "TextCompression" su "PdfTextCompression.None" per non applicare alcuna
# compressione al testo quando salviamo il documento in PDF.
# Imposta la proprietà "TextCompression" su "PdfTextCompression.Flate" per applicare la compressione ZIP
# al testo quando salviamo il documento in PDF. Più grande è il documento, maggiore sarà l'impatto di questa operazione.
options.text_compression = pdf_text_compression
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TextCompression.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

