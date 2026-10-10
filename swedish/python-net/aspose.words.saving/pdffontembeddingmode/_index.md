---
title: PdfFontEmbeddingMode enumeration
linktitle: PdfFontEmbeddingMode enumeration
articleTitle: PdfFontEmbeddingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfFontEmbeddingMode enumeration. Specifies how Aspose.Words should embed fonts."
type: docs
weight: 690
url: /sv/python-net/aspose.words.saving/pdffontembeddingmode/
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
# "Arial" är ett standardteckensnitt, och "Courier New" är ett icke‑standardteckensnitt.
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "EmbedFullFonts" till "true" för att bädda in varje glyf från varje inbäddat teckensnitt i den resulterande PDF‑filen.
options.embed_full_fonts = True
# Ställ in egenskapen "FontEmbeddingMode" till "EmbedAll" för att bädda in alla teckensnitt i den resulterande PDF‑filen.
# Ställ in egenskapen "FontEmbeddingMode" till "EmbedNonstandard" för att endast tillåta inbäddning av icke‑standardteckensnitt i den resulterande PDF‑filen.
# Ställ in egenskapen "FontEmbeddingMode" till "EmbedNone" för att inte bädda in några teckensnitt i den resulterande PDF‑filen.
options.font_embedding_mode = pdf_font_embedding_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedWindowsFonts.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

