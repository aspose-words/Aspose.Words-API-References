---
title: FixedPageSaveOptions.optimizeOutput property
linktitle: optimizeOutput property
articleTitle: optimizeOutput property
second_title: Aspose.Words for NodeJs
description: "FixedPageSaveOptions.optimizeOutput property. Flag indicates whether it is required to optimize output"
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Saving/fixedpagesaveoptions/optimizeOutput/
---

## FixedPageSaveOptions.optimizeOutput property

Flag indicates whether it is required to optimize output.
If this flag is set redundant nested canvases and empty canvases are removed,
also neighbor glyphs with the same formatting are concatenated.
Note: The accuracy of the content display may be affected if this property is set to ``True``.

Default is ``False``.



```js
get optimizeOutput(): boolean
```

### Examples

Shows how to optimize document objects while saving to xps.

```js
let doc = new aw.Document(base.myDir + "Unoptimized document.docx");

// Create an "XpsSaveOptions" object to pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
let saveOptions = new aw.Saving.XpsSaveOptions();
// Set the "OptimizeOutput" property to "true" to take measures such as removing nested or empty canvases
// and concatenating adjacent runs with identical formatting to optimize the output document's content.
// This may affect the appearance of the document.
// Set the "OptimizeOutput" property to "false" to save the document normally.
saveOptions.optimizeOutput = optimizeOutput;

doc.save(base.artifactsDir + "XpsSaveOptions.optimizeOutput.xps", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [FixedPageSaveOptions](../)

