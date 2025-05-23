﻿---
title: MarkdownSaveOptions.list_export_mode property
linktitle: list_export_mode property
articleTitle: list_export_mode property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.list_export_mode property. Specifies how list items will be written to the output file"
type: docs
weight: 110
url: /python-net/aspose.words.saving/markdownsaveoptions/list_export_mode/
---

## MarkdownSaveOptions.list_export_mode property

Specifies how list items will be written to the output file.
Default value is [MarkdownListExportMode.MARKDOWN_SYNTAX](../../markdownlistexportmode/#MARKDOWN_SYNTAX).



```python
@property
def list_export_mode(self) -> aspose.words.saving.MarkdownListExportMode:
    ...

@list_export_mode.setter
def list_export_mode(self, value: aspose.words.saving.MarkdownListExportMode):
    ...

```

### Remarks

When this property is set to [MarkdownListExportMode.PLAIN_TEXT](../../markdownlistexportmode/#PLAIN_TEXT) all list labels are
updated using [Document.update_list_labels()](../../../aspose.words/document/update_list_labels/#default) and exported with their actual values. Such lists
can be non-compatible with Markdown format and will be recognized as plain text upon importing in this case.

When this property is set to [MarkdownListExportMode.MARKDOWN_SYNTAX](../../markdownlistexportmode/#MARKDOWN_SYNTAX), writer tries to export
list items in manner that allows to numerate list items in automatic mode by Markdown.




### Examples

Shows how to list items will be written to the markdown document.

```python
doc = aw.Document(file_name=MY_DIR + 'List item.docx')
# Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
options = aw.saving.MarkdownSaveOptions()
options.list_export_mode = markdown_list_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.ListExportMode.md', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

