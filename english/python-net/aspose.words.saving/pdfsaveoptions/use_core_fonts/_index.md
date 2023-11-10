---
title: PdfSaveOptions.use_core_fonts property
linktitle: use_core_fonts property
articleTitle: use_core_fonts property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.use_core_fonts property. Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts."
type: docs
weight: 310
url: /python-net/aspose.words.saving/pdfsaveoptions/use_core_fonts/
---

## PdfSaveOptions.use_core_fonts property

Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman,
Courier New and Symbol with core PDF Type 1 fonts.


```python
@property
def use_core_fonts(self) -> bool:
    ...

@use_core_fonts.setter
def use_core_fonts(self, value: bool):
    ...

```

### Remarks

The default value is ``False``. When this value is set to ``True`` Arial, Times New Roman,
Courier New and Symbol fonts are replaced in PDF document with corresponding core Type 1 font.

Core PDF fonts, or their font metrics and suitable substitution fonts, are required to be available to any
PDF viewer application.

This setting works only for the text in ANSI (Windows-1252) encoding. Non-ANSI text will be written
with embedded TrueType font regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. ``False`` value will be used
automatically when saving to PDF/A and PDF/UA.

Core fonts are not supported when saving to PDF 2.0 format. ``False`` value will be used
automatically when saving to PDF 2.0.

This option has a higher priority then [PdfSaveOptions.font_embedding_mode](../font_embedding_mode/) option.




### Examples

Shows how enable/disable PDF Type 1 font substitution.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Arial"
builder.writeln("Hello world!")
builder.font.name = "Courier New"
builder.writeln("The quick brown fox jumps over the lazy dog.")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Set the "use_core_fonts" property to "True" to replace some fonts,
# including the two fonts in our document, with their PDF Type 1 equivalents.
# Set the "use_core_fonts" property to "False" to not apply PDF Type 1 fonts.
options.use_core_fonts = use_core_fonts

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.embed_core_fonts.pdf", options)

if use_core_fonts:
    self.assertGreater(3000, os.path.getsize(ARTIFACTS_DIR + "PdfSaveOptions.embed_core_fonts.pdf"))
else:
    self.assertLess(30000, os.path.getsize(ARTIFACTS_DIR + "PdfSaveOptions.embed_core_fonts.pdf"))
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

