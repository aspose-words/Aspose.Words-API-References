---
title: export_images_as_base64 property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB"
type: docs
weight: 180
url: /python-net/aspose.words.saving/htmlsaveoptions/export_images_as_base64/
---

## HtmlSaveOptions.export_images_as_base64 property

Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB.
Default is ``false``.


When this property is set to ``true`` images data are exported
directly into the **img** elements and separate files are not created.




### Examples

Shows how to save a .html document with images embedded inside it.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

options = aw.saving.HtmlSaveOptions()
options.export_images_as_base64 = export_items_as_base64
options.pretty_format = True

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.export_images_as_base64.html", options)

with open(ARTIFACTS_DIR + "HtmlSaveOptions.export_images_as_base64.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if export_items_as_base64:
    self.assertIn("<img src=\"data:image/png;base64", out_doc_contents)
else:
    self.assertIn("<img src=\"HtmlSaveOptions.export_images_as_base64.001.png\"", out_doc_contents)
```

Shows how to embed fonts inside a saved HTML document.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

options = aw.saving.HtmlSaveOptions()
options.export_fonts_as_base64 = True
options.css_style_sheet_type = aw.saving.CssStyleSheetType.EMBEDDED
options.pretty_format = True

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.export_fonts_as_base64.html", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

