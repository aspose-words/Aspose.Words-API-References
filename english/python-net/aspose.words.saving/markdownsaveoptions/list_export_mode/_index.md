---
title: list_export_mode property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies how list items will be written to the output file"
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




### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

