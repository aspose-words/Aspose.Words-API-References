---
title: MarkdownListExportMode enumeration
linktitle: MarkdownListExportMode enumeration
articleTitle: MarkdownListExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.MarkdownListExportMode enumeration. Specifies how lists are exported into Markdown."
type: docs
weight: 450
url: /python-net/aspose.words.saving/markdownlistexportmode/
---

## MarkdownListExportMode enumeration

Specifies how lists are exported into Markdown.


### Members

| Name | Description |
| --- | --- |
| MARKDOWN_SYNTAX | Export list items compatible with Markdown syntax. |
| PLAIN_TEXT | Export list items as plain text. |

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

* module [aspose.words.saving](../)

