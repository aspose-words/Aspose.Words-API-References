---
title: MarkdownListExportMode enumeration
linktitle: MarkdownListExportMode enumeration
articleTitle: MarkdownListExportMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.MarkdownListExportMode enumeration. Specifies how lists are exported into Markdown."
type: docs
weight: 430
url: /nodejs-net/aspose.words.saving/markdownlistexportmode/
---

## MarkdownListExportMode enumeration

Specifies how lists are exported into Markdown.


### Members

| Name | Description |
| --- | --- |
| MarkdownSyntax | Export list items compatible with Markdown syntax. |
| PlainText | Export list items as plain text. |

### Examples

Shows how to list items will be written to the markdown document.

```js
let doc = new aw.Document(base.myDir + "List item.docx");

// Use MarkdownListExportMode.PlainText or MarkdownListExportMode.MarkdownSyntax to export list.
let options = new aw.Saving.MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.save(base.artifactsDir + "MarkdownSaveOptions.listExportMode.md", options);
```

### See Also

* module [Aspose.Words.Saving](../)

