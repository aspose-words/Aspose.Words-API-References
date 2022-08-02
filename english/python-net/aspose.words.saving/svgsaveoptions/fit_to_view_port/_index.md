---
title: fit_to_view_port property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies if the output SVG should fill the available viewport area (browser window or container)"
type: docs
weight: 30
url: /python-net/aspose.words.saving/svgsaveoptions/fit_to_view_port/
---

## SvgSaveOptions.fit_to_view_port property

Specifies if the output SVG should fill the available viewport area (browser window or container).
When set to true width and height of output SVG are set to 100%.

The default value is false.




### Examples

Shows how to mimic the properties of images when converting a .docx document to .svg.

```python
doc = aw.Document(MY_DIR + "Document.docx")

# Configure the SvgSaveOptions object to save with no page borders or selectable text.
options = aw.saving.SvgSaveOptions()
options.fit_to_view_port = True
options.show_page_border = False
options.text_output_mode = aw.saving.SvgTextOutputMode.USE_PLACED_GLYPHS

doc.save(ARTIFACTS_DIR + "SvgSaveOptions.save_like_image.svg", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SvgSaveOptions](../)

