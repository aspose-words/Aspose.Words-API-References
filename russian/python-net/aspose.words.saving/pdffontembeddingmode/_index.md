---
title: PdfFontEmbeddingMode enumeration
linktitle: PdfFontEmbeddingMode enumeration
articleTitle: PdfFontEmbeddingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfFontEmbeddingMode enumeration. Specifies how Aspose.Words should embed fonts."
type: docs
weight: 690
url: /ru/python-net/aspose.words.saving/pdffontembeddingmode/
---

## PdfFontEmbeddingMode enumeration

Specifies how Aspose.Words should embed fonts.


### Members

| Name | Description |
| --- | --- |
| EMBED_ALL | Aspose.Words embeds all fonts. |
| EMBED_NONSTANDARD | Aspose.Words embeds all fonts excepting standard Windows fonts Arial and Times New Roman. Only Arial and Times New Roman fonts are affected in this mode because MS Word doesn't embed only these fonts when saving document to PDF. |
| EMBED_NONE | Aspose.Words do not embed any fonts. |

### Examples

Shows how to set Aspose.Words to skip embedding Arial and Times New Roman fonts into a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# "Arial" — стандартный шрифт, а "Courier New" — нестандартный шрифт.
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Установите свойство "EmbedFullFonts" в значение "true", чтобы внедрить каждый глиф каждого встроенного шрифта в выходной PDF.
options.embed_full_fonts = True
# Установите свойство "FontEmbeddingMode" в значение "EmbedAll", чтобы внедрить все шрифты в выходной PDF.
# Установите свойство "FontEmbeddingMode" в значение "EmbedNonstandard", чтобы разрешить внедрение только нестандартных шрифтов в выходной PDF.
# Установите свойство "FontEmbeddingMode" в значение "EmbedNone", чтобы не внедрять никакие шрифты в выходной PDF.
options.font_embedding_mode = pdf_font_embedding_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedWindowsFonts.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

