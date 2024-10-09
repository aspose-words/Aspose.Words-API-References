---
title: MarkdownLinkExportMode enumeration
linktitle: MarkdownLinkExportMode enumeration
articleTitle: MarkdownLinkExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.MarkdownLinkExportMode enumeration. Specifies how links are exported into Markdown."
type: docs
weight: 430
url: /python-net/aspose.words.saving/markdownlinkexportmode/
---

## MarkdownLinkExportMode enumeration

Specifies how links are exported into Markdown.


### Members

| Name | Description |
| --- | --- |
| AUTO | Automatically detect export mode for each link. |
| INLINE | Export all links as inline blocks. |
| REFERENCE | Export all links as reference blocks. |

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

* module [aspose.words.saving](../)

