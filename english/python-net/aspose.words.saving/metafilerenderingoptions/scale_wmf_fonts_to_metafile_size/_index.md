---
title: MetafileRenderingOptions.scale_wmf_fonts_to_metafile_size property
linktitle: scale_wmf_fonts_to_metafile_size property
articleTitle: scale_wmf_fonts_to_metafile_size property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.scale_wmf_fonts_to_metafile_size property. Gets or sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page."
type: docs
weight: 50
url: /python-net/aspose.words.saving/metafilerenderingoptions/scale_wmf_fonts_to_metafile_size/
---

## MetafileRenderingOptions.scale_wmf_fonts_to_metafile_size property

Gets or sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page.

When WMF metafiles are displayed in MS Word, fonts may be scaled according to actual metafile size on the page.

When this value is set to ``True``, Aspose.Words emulates font scaling according to metafile size on the page.

When this value is set to ``False``, Aspose.Words displays the fonts as metafile is rendered to its default size.

This option is used only when metafile is rendered as vector graphics.

The default value is ``True``.




### Examples

Shows how to WMF fonts scaling according to metafile size on the page.

```python
doc = aw.Document(MY_DIR + "WMF with text.docx")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()

# Set the "scale_wmf_fonts_to_metafile_size" property to "True" to scale fonts
# that format text within WMF images according to the size of the metafile on the page.
# Set the "scale_wmf_fonts_to_metafile_size" property to "False" to
# preserve the default scale of these fonts.
save_options.metafile_rendering_options.scale_wmf_fonts_to_metafile_size = scale_wmf_fonts

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.fonts_scaled_to_metafile_size.pdf", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

