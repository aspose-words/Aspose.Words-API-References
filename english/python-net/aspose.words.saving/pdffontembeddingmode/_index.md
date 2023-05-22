---
title: PdfFontEmbeddingMode enumeration
linktitle: PdfFontEmbeddingMode enumeration
articleTitle: PdfFontEmbeddingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfFontEmbeddingMode enumeration. Specifies how Aspose.Words should embed fonts."
type: docs
weight: 620
url: /python-net/aspose.words.saving/pdffontembeddingmode/
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
builder = aw.DocumentBuilder(doc)

# "Arial" is a standard font, and "Courier New" is a nonstandard font.
builder.font.name = "Arial"
builder.writeln("Hello world!")
builder.font.name = "Courier New"
builder.writeln("The quick brown fox jumps over the lazy dog.")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Set the "embed_full_fonts" property to "True" to embed every glyph of every embedded font in the output PDF.
options.embed_full_fonts = True

# Set the "font_embedding_mode" property to "EMBED_ALL" to embed all fonts in the output PDF.
# Set the "font_embedding_mode" property to "EMBED_NONSTANDARD" to only allow nonstandard fonts' embedding in the output PDF.
# Set the "font_embedding_mode" property to "EMBED_NONE" to not embed any fonts in the output PDF.
options.font_embedding_mode = pdf_font_embedding_mode

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.embed_windows_fonts.pdf", options)

if pdf_font_embedding_mode == aw.saving.PdfFontEmbeddingMode.EMBED_ALL:
    self.assertLess(1000000, os.path.getsize(ARTIFACTS_DIR + "PdfSaveOptions.embed_windows_fonts.pdf"))

elif pdf_font_embedding_mode == aw.saving.PdfFontEmbeddingMode.EMBED_NONSTANDARD:
    self.assertLess(480000, os.path.getsize(ARTIFACTS_DIR + "PdfSaveOptions.embed_windows_fonts.pdf"))

elif pdf_font_embedding_mode == aw.saving.PdfFontEmbeddingMode.EMBED_NONE:
    self.assertGreater(4243, os.path.getsize(ARTIFACTS_DIR + "PdfSaveOptions.embed_windows_fonts.pdf"))
```

### See Also

* module [aspose.words.saving](../)

