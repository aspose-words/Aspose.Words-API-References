---
title: MarkdownOfficeMathExportMode enumeration
linktitle: MarkdownOfficeMathExportMode enumeration
articleTitle: MarkdownOfficeMathExportMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.MarkdownOfficeMathExportMode enumeration. Specifies how Aspose.Words exports OfficeMath to Markdown."
type: docs
weight: 440
url: /nodejs-net/aspose.words.saving/markdownofficemathexportmode/
---

## MarkdownOfficeMathExportMode enumeration

Specifies how Aspose.Words exports OfficeMath to Markdown.


### Members

| Name | Description |
| --- | --- |
| Text | Export OfficeMath as plain text. |
| Image | Export OfficeMath as image. |
| MathML | Export OfficeMath as MathML. |

### Examples

Shows how OfficeMath will be written to the document.

```js
let doc = new aw.Document(base.myDir + "Office math.docx");

let saveOptions = new aw.Saving.MarkdownSaveOptions();
saveOptions.officeMathExportMode = aw.Saving.MarkdownOfficeMathExportMode.Image;

doc.save(base.artifactsDir + "MarkdownSaveOptions.officeMathExportMode.md", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)

