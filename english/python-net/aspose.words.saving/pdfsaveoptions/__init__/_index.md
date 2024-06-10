---
title: PdfSaveOptions constructor
linktitle: PdfSaveOptions constructor
articleTitle: PdfSaveOptions constructor
second_title: Aspose.Words for Python
description: "PdfSaveOptions constructor. Initializes a new instance of this class that can be used to save a document in the [SaveFormat.PDF](../../../aspose.words/saveformat/#PDF) format."
type: docs
weight: 10
url: /python-net/aspose.words.saving/pdfsaveoptions/__init__/
---

## PdfSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document in the
[SaveFormat.PDF](../../../aspose.words/saveformat/#PDF) format.



```python
def __init__(self):
    ...
```

### Examples

Shows how to enable or disable subsetting when embedding fonts while rendering a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Arvo'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# Configure our font sources to ensure that we have access to both the fonts in this document.
original_fonts_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
folder_font_source = aw.fonts.FolderFontSource(FONTS_DIR, True)
aw.fonts.FontSettings.default_instance.set_fonts_sources([original_fonts_sources[0], folder_font_source])
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
self.assertTrue(any((font.full_font_name == 'Arial' for font in font_sources[0].get_available_fonts())))
self.assertTrue(any((font.full_font_name == 'Arvo' for font in font_sources[1].get_available_fonts())))
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Since our document contains a custom font, embedding in the output document may be desirable.
# Set the "embed_full_fonts" property to "True" to embed every glyph of every embedded font in the output PDF.
# The document's size may become very large, but we will have full use of all fonts if we edit the PDF.
# Set the "embed_full_fonts" property to "False" to apply subsetting to fonts, saving only the glyphs
# that the document is using. The file will be considerably smaller,
# but we may need access to any custom fonts if we edit the document.
options.embed_full_fonts = embed_full_fonts
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.embed_full_fonts.pdf', options)
if embed_full_fonts:
    self.assertLess(500000, os.path.getsize(ARTIFACTS_DIR + 'PdfSaveOptions.embed_full_fonts.pdf'))
else:
    self.assertGreater(25000, os.path.getsize(ARTIFACTS_DIR + 'PdfSaveOptions.embed_full_fonts.pdf'))
# Restore the original font sources.
aw.fonts.FontSettings.default_instance.set_fonts_sources(original_fonts_sources)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

