---
title: MarkdownSaveOptions.image_resolution property
linktitle: image_resolution property
articleTitle: image_resolution property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.image_resolution property. Specifies the output resolution for images when exporting to Markdown"
type: docs
weight: 50
url: /python-net/aspose.words.saving/markdownsaveoptions/image_resolution/
---

## MarkdownSaveOptions.image_resolution property

Specifies the output resolution for images when exporting to Markdown.
Default is ``96 dpi``.



```python
@property
def image_resolution(self) -> int:
    ...

@image_resolution.setter
def image_resolution(self, value: int):
    ...

```

### Examples

Shows how to set the output resolution for images.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.MarkdownSaveOptions()
save_options.image_resolution = 300
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.ImageResolution.md', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

