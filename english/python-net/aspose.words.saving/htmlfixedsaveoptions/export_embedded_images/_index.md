---
title: HtmlFixedSaveOptions.export_embedded_images property
linktitle: export_embedded_images property
articleTitle: export_embedded_images property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.export_embedded_images property. Specifies whether images should be embedded into Html document in Base64 format"
type: docs
weight: 60
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/export_embedded_images/
---

## HtmlFixedSaveOptions.export_embedded_images property

Specifies whether images should be embedded into Html document in Base64 format.
Note setting this flag can significantly increase size of output Html file.


```python
@property
def export_embedded_images(self) -> bool:
    ...

@export_embedded_images.setter
def export_embedded_images(self, value: bool):
    ...

```

### Examples

Shows how to determine where to store images when exporting a document to Html.

```python
doc = aw.Document(MY_DIR + 'Images.docx')
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.export_embedded_images = export_images
doc.save(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedImages.html', save_options=html_fixed_save_options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedImages.html')
if export_images:
    self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg'))
    self.assertTrue(re.match('<img class=\\"awimg\\" style=\\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\\" src=\\".+\\" />', out_doc_contents))
else:
    self.assertTrue(system_helper.io.File.exist(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg'))
    self.assertTrue(re.match('<img class=\\"awimg\\" style=\\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\\" src=\\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\\" />', out_doc_contents))
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

