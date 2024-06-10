---
title: HtmlSaveOptions.export_images_as_base64 property
linktitle: export_images_as_base64 property
articleTitle: export_images_as_base64 property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_images_as_base64 property. Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB"
type: docs
weight: 170
url: /python-net/aspose.words.saving/htmlsaveoptions/export_images_as_base64/
---

## HtmlSaveOptions.export_images_as_base64 property

Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB.
Default is ``False``.



```python
@property
def export_images_as_base64(self) -> bool:
    ...

@export_images_as_base64.setter
def export_images_as_base64(self, value: bool):
    ...

```

### Remarks

When this property is set to ``True`` images data are exported
directly into the **img** elements and separate files are not created.




### Examples

Shows how to embed fonts inside a saved HTML document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
options = aw.saving.HtmlSaveOptions()
options.export_fonts_as_base64 = True
options.css_style_sheet_type = aw.saving.CssStyleSheetType.EMBEDDED
options.pretty_format = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ExportFontsAsBase64.html', save_options=options)
```

Shows how to save a .html document with images embedded inside it.

```python
doc = aw.Document(MY_DIR + 'Rendering.docx')
options = aw.saving.HtmlSaveOptions()
options.export_images_as_base64 = export_images_as_base64
options.pretty_format = True
doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.export_images_as_base64.html', options)
with open(ARTIFACTS_DIR + 'HtmlSaveOptions.export_images_as_base64.html', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
if export_images_as_base64:
    self.assertIn('<img src="data:image/png;base64', out_doc_contents)
else:
    self.assertIn('<img src="HtmlSaveOptions.export_images_as_base64.001.png"', out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

