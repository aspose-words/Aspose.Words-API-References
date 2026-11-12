---
title: PdfTextCompression enumeration
linktitle: PdfTextCompression enumeration
articleTitle: PdfTextCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfTextCompression enumeration. Specifies a type of compression applied to all content in the PDF file except images."
type: docs
weight: 760
url: /tr/python-net/aspose.words.saving/pdftextcompression/
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
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
options = aw.saving.PdfSaveOptions()
# "TextCompression" özelliğini "PdfTextCompression.None" olarak ayarlayın, böylece herhangi bir
# metin sıkıştırması uygulanmaz, belgeyi PDF olarak kaydederken.
# "TextCompression" özelliğini "PdfTextCompression.Flate" olarak ayarlayın, ZIP sıkıştırması uygulamak için
# belgeyi PDF olarak kaydederken metne. Belge ne kadar büyükse, bu durumun etkisi o kadar büyük olur.
options.text_compression = pdf_text_compression
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TextCompression.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

