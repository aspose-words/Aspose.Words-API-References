---
title: PdfSaveOptions.text_compression property
linktitle: text_compression property
articleTitle: text_compression property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.text_compression property. Specifies compression type to be used for all textual content in the document."
type: docs
weight: 330
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/text_compression/
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
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "TextCompression" till "PdfTextCompression.None" för att inte tillämpa någon
# komprimering på text när vi sparar dokumentet till PDF.
# Ställ in egenskapen "TextCompression" till "PdfTextCompression.Flate" för att tillämpa ZIP-komprimering
# på text när vi sparar dokumentet till PDF. Ju större dokumentet är, desto större påverkan får detta.
options.text_compression = pdf_text_compression
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TextCompression.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

