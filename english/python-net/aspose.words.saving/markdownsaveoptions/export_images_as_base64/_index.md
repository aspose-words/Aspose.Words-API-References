---
title: export_images_as_base64 property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether images are saved in Base64 format to the output file"
type: docs
weight: 20
url: /python-net/aspose.words.saving/markdownsaveoptions/export_images_as_base64/
---

## MarkdownSaveOptions.export_images_as_base64 property

Specifies whether images are saved in Base64 format to the output file.
Default is ``False``.


When this property is set to ``True`` images data are exported
directly into the **img** elements and separate files are not created.




### Examples

Shows how to save a .md document with images embedded inside it.

```python
doc = aw.Document(MY_DIR + "Images.docx")

save_options = aw.saving.MarkdownSaveOptions()
save_options.export_images_as_base64 = export_images_as_base64

doc.save(ARTIFACTS_DIR + "MarkdownSaveOptions.ExportImagesAsBase64.md", save_options)

with open(ARTIFACTS_DIR + "MarkdownSaveOptions.ExportImagesAsBase64.md") as stream:
    out_doc_contents = stream.read()

if export_images_as_base64:
    self.assertIn("data:image/jpeg;base64", out_doc_contents)
else:
    self.assertIn("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg", out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

