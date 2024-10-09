---
title: SvgTextOutputMode enumeration
linktitle: SvgTextOutputMode enumeration
articleTitle: SvgTextOutputMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.SvgTextOutputMode enumeration. Allows to specify how text inside a document should be rendered when saving in SVG format."
type: docs
weight: 790
url: /python-net/aspose.words.saving/svgtextoutputmode/
---

## SvgTextOutputMode enumeration

Allows to specify how text inside a document should be rendered
when saving in SVG format.


### Members

| Name | Description |
| --- | --- |
| USE_SVG_FONTS | SVG fonts are used to render text. Note, not all browsers support SVG fonts. |
| USE_TARGET_MACHINE_FONTS | Fonts installed on the target machine are used to render text.  Note, if some of fonts used in the document are not available on the target machine, document can look differently. |
| USE_PLACED_GLYPHS | Text is rendered using curves. Note, text selection will not work if you use this option. |

### Examples

Shows how to mimic the properties of images when converting a .docx document to .svg.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
# Configure the SvgSaveOptions object to save with no page borders or selectable text.
options = aw.saving.SvgSaveOptions()
options.fit_to_view_port = True
options.show_page_border = False
options.text_output_mode = aw.saving.SvgTextOutputMode.USE_PLACED_GLYPHS
doc.save(file_name=ARTIFACTS_DIR + 'SvgSaveOptions.SaveLikeImage.svg', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

