---
title: MarkdownSaveOptions.list_export_mode property
linktitle: list_export_mode property
articleTitle: list_export_mode property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.list_export_mode property. Specifies how list items will be written to the output file"
type: docs
weight: 50
url: /python-net/aspose.words.saving/markdownsaveoptions/list_export_mode/
---

## MarkdownSaveOptions.list_export_mode property

Specifies how list items will be written to the output file.
Default value is [MarkdownListExportMode.MARKDOWN_SYNTAX](../../markdownlistexportmode/#MARKDOWN_SYNTAX).


When this property is set to [MarkdownListExportMode.PLAIN_TEXT](../../markdownlistexportmode/#PLAIN_TEXT) all list labels are
updated using [Document.update_list_labels()](../../../aspose.words/document/update_list_labels/#default) and exported with their actual values. Such lists
can be non-compatible with Markdown format and will be recognized as plain text upon importing in this case.

When this property is set to [MarkdownListExportMode.MARKDOWN_SYNTAX](../../markdownlistexportmode/#MARKDOWN_SYNTAX), writer tries to export
list items in manner that allows to numerate list items in automatic mode by Markdown.




### Examples

Shows how to list items will be written to the markdown document.

```python
doc = aw.Document(MY_DIR + "List item.docx");

# Use MarkdownListExportMode.PLAIN_TEXT or MarkdownListExportMode.MARKDOWN_SYNTAX to export list.
options = aw.saving.MarkdownSaveOptions()
options.list_export_mode = markdownListExportMode
doc.save(ARTIFACTS_DIR + "MarkdownSaveOptions.ListExportMode.md", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

