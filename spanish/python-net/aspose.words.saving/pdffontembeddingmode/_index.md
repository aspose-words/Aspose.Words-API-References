---
title: PdfFontEmbeddingMode enumeration
linktitle: PdfFontEmbeddingMode enumeration
articleTitle: PdfFontEmbeddingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfFontEmbeddingMode enumeration. Specifies how Aspose.Words should embed fonts."
type: docs
weight: 690
url: /es/python-net/aspose.words.saving/pdffontembeddingmode/
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
# "Arial" es una fuente estándar, y "Courier New" es una fuente no estándar.
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# Establezca la propiedad "EmbedFullFonts" a "true" para incrustar cada glifo de todas las fuentes incrustadas en el PDF de salida.
options.embed_full_fonts = True
# Establezca la propiedad "FontEmbeddingMode" a "EmbedAll" para incrustar todas las fuentes en el PDF de salida.
# Establezca la propiedad "FontEmbeddingMode" a "EmbedNonstandard" para permitir únicamente la incrustación de fuentes no estándar en el PDF de salida.
# Establezca la propiedad "FontEmbeddingMode" a "EmbedNone" para no incrustar ninguna fuente en el PDF de salida.
options.font_embedding_mode = pdf_font_embedding_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedWindowsFonts.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

