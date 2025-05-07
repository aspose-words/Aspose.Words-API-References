---
title: MarkdownSaveOptions.officeMathExportMode property
linktitle: officeMathExportMode property
articleTitle: officeMathExportMode property
second_title: Aspose.Words for Node.js
description: "MarkdownSaveOptions.officeMathExportMode property. Specifies how OfficeMath will be written to the output file"
type: docs
weight: 120
url: /nodejs-net/aspose.words.saving/markdownsaveoptions/officeMathExportMode/
---

## MarkdownSaveOptions.officeMathExportMode property

Specifies how OfficeMath will be written to the output file.
Default value is [MarkdownOfficeMathExportMode.Text](../../markdownofficemathexportmode/#Text).



```js
get officeMathExportMode(): Aspose.Words.Saving.MarkdownOfficeMathExportMode
```

### Examples

Shows how OfficeMath will be written to the document.

```js
let doc = new aw.Document(base.myDir + "Office math.docx");

let saveOptions = new aw.Saving.MarkdownSaveOptions();
saveOptions.officeMathExportMode = aw.Saving.MarkdownOfficeMathExportMode.Image;

doc.save(base.artifactsDir + "MarkdownSaveOptions.officeMathExportMode.md", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)

