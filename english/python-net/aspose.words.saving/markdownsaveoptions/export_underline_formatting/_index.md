---
title: MarkdownSaveOptions.export_underline_formatting property
linktitle: export_underline_formatting property
articleTitle: export_underline_formatting property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.export_underline_formatting property. Gets or sets a boolean value indicating either to export underline text formatting as sequence of two plus characters ++"
type: docs
weight: 50
url: /python-net/aspose.words.saving/markdownsaveoptions/export_underline_formatting/
---

## MarkdownSaveOptions.export_underline_formatting property

Gets or sets a boolean value indicating either to export underline
text formatting as sequence of two plus characters "++".
The default value is ``False``.



```python
@property
def export_underline_formatting(self) -> bool:
    ...

@export_underline_formatting.setter
def export_underline_formatting(self, value: bool):
    ...

```

### Examples

Shows how to export underline formatting as ++.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.underline = aw.Underline.SINGLE
builder.write('Lorem ipsum. Dolor sit amet.')
save_options = aw.saving.MarkdownSaveOptions()
save_options.export_underline_formatting = True
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.ExportUnderlineFormatting.md', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

