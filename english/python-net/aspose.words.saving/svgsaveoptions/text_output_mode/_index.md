---
title: text_output_mode property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a value determining how text should be rendered in SVG."
type: docs
weight: 90
url: /python-net/aspose.words.saving/svgsaveoptions/text_output_mode/
---

## SvgSaveOptions.text_output_mode property

Gets or sets a value determining how text should be rendered in SVG.

Use this property to get or set the mode of how text inside a document should be rendered
when saving in SVG format.

The default value is [SvgTextOutputMode.USE_TARGET_MACHINE_FONTS](../../svgtextoutputmode/#USE_TARGET_MACHINE_FONTS).




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

