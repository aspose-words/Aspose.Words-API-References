---
title: MarkdownSaveOptions.export_images_as_base64 property
linktitle: export_images_as_base64 property
articleTitle: export_images_as_base64 property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.export_images_as_base64 property. Specifies whether images are saved in Base64 format to the output file"
type: docs
weight: 40
url: /python-net/aspose.words.saving/markdownsaveoptions/export_images_as_base64/
---

## MarkdownSaveOptions.export_images_as_base64 property

Specifies whether images are saved in Base64 format to the output file.
Default value is ``False``.



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

Shows how to save a .md document with images embedded inside it.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
save_options = aw.saving.MarkdownSaveOptions()
save_options.export_images_as_base64 = export_images_as_base64
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.ExportImagesAsBase64.md', save_options=save_options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'MarkdownSaveOptions.ExportImagesAsBase64.md')
self.assertTrue('data:image/jpeg;base64' in out_doc_contents if export_images_as_base64 else 'MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

