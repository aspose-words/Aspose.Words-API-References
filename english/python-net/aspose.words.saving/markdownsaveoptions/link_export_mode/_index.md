---
title: MarkdownSaveOptions.link_export_mode property
linktitle: link_export_mode property
articleTitle: link_export_mode property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.link_export_mode property. Specifies how links will be written to the output file"
type: docs
weight: 90
url: /python-net/aspose.words.saving/markdownsaveoptions/link_export_mode/
---

## MarkdownSaveOptions.link_export_mode property

Specifies how links will be written to the output file.
Default value is [MarkdownLinkExportMode.AUTO](../../markdownlinkexportmode/#AUTO).



```python
@property
def link_export_mode(self) -> aspose.words.saving.MarkdownLinkExportMode:
    ...

@link_export_mode.setter
def link_export_mode(self, value: aspose.words.saving.MarkdownLinkExportMode):
    ...

```

### Examples

Shows how to links will be written to the .md file.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_shape(shape_type=aw.drawing.ShapeType.BALLOON, width=100, height=100)
# Image will be written as reference:
# ![ref1]
#
# [ref1]: aw_ref.001.png
save_options = aw.saving.MarkdownSaveOptions()
save_options.link_export_mode = aw.saving.MarkdownLinkExportMode.REFERENCE
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.LinkExportMode.Reference.md', save_options=save_options)
# Image will be written as inline:
# ![](aw_inline.001.png)
save_options.link_export_mode = aw.saving.MarkdownLinkExportMode.INLINE
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.LinkExportMode.Inline.md', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

