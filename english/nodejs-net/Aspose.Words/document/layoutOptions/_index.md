---
title: Document.layoutOptions property
linktitle: layoutOptions property
articleTitle: layoutOptions property
second_title: Aspose.Words for Node.js
description: "Document.layoutOptions property. Gets a [LayoutOptions](../../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document."
type: docs
weight: 260
url: /nodejs-net/aspose.words/document/layoutOptions/
---

## Document.layoutOptions property

Gets a [LayoutOptions](../../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document.



```js
get layoutOptions(): Aspose.Words.Layout.LayoutOptions
```

### Examples

Shows how to alter the appearance of revisions in a rendered output document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a revision, then change the color of all revisions to green.
builder.writeln("This is not a revision.");
doc.startTrackRevisions("John Doe", Date.now());
expect(doc.layoutOptions.revisionOptions.insertedTextColor).toEqual(aw.Layout.RevisionColor.ByAuthor);
expect(doc.layoutOptions.revisionOptions.showRevisionBars).toEqual(true);
builder.writeln("This is a revision.");
doc.stopTrackRevisions();
builder.writeln("This is not a revision.");

// Remove the bar that appears to the left of every revised line.
doc.layoutOptions.revisionOptions.insertedTextColor = aw.Layout.RevisionColor.BrightGreen;
doc.layoutOptions.revisionOptions.showRevisionBars = false;
doc.layoutOptions.revisionOptions.revisionBarsPosition = aw.Drawing.HorizontalAlignment.Right;

doc.save(base.artifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

