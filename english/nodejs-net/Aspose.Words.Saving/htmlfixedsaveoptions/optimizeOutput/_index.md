---
title: HtmlFixedSaveOptions.optimizeOutput property
linktitle: optimizeOutput property
articleTitle: optimizeOutput property
second_title: Aspose.Words for Node.js
description: "HtmlFixedSaveOptions.optimizeOutput property. Flag indicates whether it is required to optimize output"
type: docs
weight: 110
url: /nodejs-net/aspose.words.saving/htmlfixedsaveoptions/optimizeOutput/
---

## HtmlFixedSaveOptions.optimizeOutput property

Flag indicates whether it is required to optimize output.
If this flag is set redundant nested canvases and empty canvases are removed,
also neighbor glyphs with the same formating are concatenated.
Note: The accuracy of the content display may be affected if this property is set to ``true``.

Default is ``true``.



```js
get optimizeOutput(): boolean
```

### Examples

Shows how to simplify a document when saving it to HTML by removing various redundant objects.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let saveOptions = new aw.Saving.HtmlFixedSaveOptions();
saveOptions.optimizeOutput = optimizeOutput;

doc.save(base.artifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// The size of the optimized version of the document is almost a third of the size of the unoptimized document.
expect(Math.abs(fs.statSync(base.artifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").size - (optimizeOutput ? 61889 : 191000))).toBeLessThanOrEqual(200);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

