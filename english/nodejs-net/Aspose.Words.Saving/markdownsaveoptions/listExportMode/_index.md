﻿---
title: MarkdownSaveOptions.listExportMode property
linktitle: listExportMode property
articleTitle: listExportMode property
second_title: Aspose.Words for Node.js
description: "MarkdownSaveOptions.listExportMode property. Specifies how list items will be written to the output file"
type: docs
weight: 110
url: /nodejs-net/aspose.words.saving/markdownsaveoptions/listExportMode/
---

## MarkdownSaveOptions.listExportMode property

Specifies how list items will be written to the output file.
Default value is [MarkdownListExportMode.MarkdownSyntax](../../markdownlistexportmode/#MarkdownSyntax).



```js
get listExportMode(): Aspose.Words.Saving.MarkdownListExportMode
```

### Remarks

When this property is set to [MarkdownListExportMode.PlainText](../../markdownlistexportmode/#PlainText) all list labels are
updated using [Document.updateListLabels()](../../../aspose.words/document/updateListLabels/#default) and exported with their actual values. Such lists
can be non-compatible with Markdown format and will be recognized as plain text upon importing in this case.

When this property is set to [MarkdownListExportMode.MarkdownSyntax](../../markdownlistexportmode/#MarkdownSyntax), writer tries to export
list items in manner that allows to numerate list items in automatic mode by Markdown.




### See Also

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)

