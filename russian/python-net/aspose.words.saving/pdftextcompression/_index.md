---
title: PdfTextCompression enumeration
linktitle: PdfTextCompression enumeration
articleTitle: PdfTextCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfTextCompression enumeration. Specifies a type of compression applied to all content in the PDF file except images."
type: docs
weight: 760
url: /ru/python-net/aspose.words.saving/pdftextcompression/
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
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Установите свойство "TextCompression" в "PdfTextCompression.None", чтобы не применять
# сжатие текста при сохранении документа в PDF.
# Установите свойство "TextCompression" в "PdfTextCompression.Flate", чтобы применить ZIP‑сжатие
# к тексту при сохранении документа в PDF. Чем больше документ, тем сильнее будет влияние этого.
options.text_compression = pdf_text_compression
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TextCompression.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

