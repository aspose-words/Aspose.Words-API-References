---
title: PdfSaveOptions.font_embedding_mode property
linktitle: font_embedding_mode property
articleTitle: font_embedding_mode property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.font_embedding_mode property. Specifies the font embedding mode."
type: docs
weight: 170
url: /python-net/aspose.words.saving/pdfsaveoptions/font_embedding_mode/
---

## PdfSaveOptions.font_embedding_mode property

Specifies the font embedding mode.


```python
@property
def font_embedding_mode(self) -> aspose.words.saving.PdfFontEmbeddingMode:
    ...

@font_embedding_mode.setter
def font_embedding_mode(self, value: aspose.words.saving.PdfFontEmbeddingMode):
    ...

```

### Remarks

The default value is [PdfFontEmbeddingMode.EMBED_ALL](../../pdffontembeddingmode/#EMBED_ALL).

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains
non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded.
[PdfFontEmbeddingMode.EMBED_ALL](../../pdffontembeddingmode/#EMBED_ALL) value will be used automatically when saving to
PDF/A and PDF/UA.




### Examples

Shows how to set Aspose.Words to skip embedding Arial and Times New Roman fonts into a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# "Arial" is a standard font, and "Courier New" is a nonstandard font.
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Set the "EmbedFullFonts" property to "true" to embed every glyph of every embedded font in the output PDF.
options.embed_full_fonts = True
# Set the "FontEmbeddingMode" property to "EmbedAll" to embed all fonts in the output PDF.
# Set the "FontEmbeddingMode" property to "EmbedNonstandard" to only allow nonstandard fonts' embedding in the output PDF.
# Set the "FontEmbeddingMode" property to "EmbedNone" to not embed any fonts in the output PDF.
options.font_embedding_mode = pdf_font_embedding_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedWindowsFonts.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

