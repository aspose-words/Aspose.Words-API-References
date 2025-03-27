---
title: TxtSaveOptionsBase.forcePageBreaks property
linktitle: forcePageBreaks property
articleTitle: forcePageBreaks property
second_title: Aspose.Words for NodeJs
description: "TxtSaveOptionsBase.forcePageBreaks property. Allows to specify whether the page breaks should be preserved during export."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/txtsaveoptionsbase/forcePageBreaks/
---

## TxtSaveOptionsBase.forcePageBreaks property

Allows to specify whether the page breaks should be preserved during export.

The default value is ``False``.




```js
get forcePageBreaks(): boolean
```

### Remarks

The property affects only page breaks that are inserted explicitly into a document. 
It is not related to page breaks that MS Word automatically inserts at the end of each page.


### Examples

Shows how to specify whether to preserve page breaks when exporting a document to plaintext.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Page 1");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 2");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 3");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save"
// method to modify how we save the document to plaintext.
let saveOptions = new aw.Saving.TxtSaveOptions();

// The Aspose.words "Document" objects have page breaks, just like Microsoft Word documents.
// Save formats such as ".txt" are one continuous body of text without page breaks.
// Set the "ForcePageBreaks" property to "true" to preserve all page breaks in the form of '\f' characters.
// Set the "ForcePageBreaks" property to "false" to discard all page breaks.
saveOptions.forcePageBreaks = forcePageBreaks;

doc.save(base.artifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// If we load a plaintext document with page breaks,
// the "Document" object will use them to split the body into pages.
doc = new aw.Document(base.artifactsDir + "TxtSaveOptions.PageBreaks.txt");

expect(doc.pageCount).toEqual(forcePageBreaks ? 3 : 1);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [TxtSaveOptionsBase](../)

