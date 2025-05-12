---
title: RevisionOptions.revisionBarsPosition property
linktitle: revisionBarsPosition property
articleTitle: revisionBarsPosition property
second_title: Aspose.Words for Node.js
description: "RevisionOptions.revisionBarsPosition property. Gets or sets rendering position of revision bars"
type: docs
weight: 160
url: /nodejs-net/aspose.words.layout/revisionoptions/revisionBarsPosition/
---

## RevisionOptions.revisionBarsPosition property

Gets or sets rendering position of revision bars.
Default value is [HorizontalAlignment.Outside](../../../aspose.words.drawing/horizontalalignment/#Outside).



```js
get revisionBarsPosition(): Aspose.Words.Drawing.HorizontalAlignment
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Values of [HorizontalAlignment.Center](../../../aspose.words.drawing/horizontalalignment/#Center) and [HorizontalAlignment.Inside](../../../aspose.words.drawing/horizontalalignment/#Inside)  are not allowed. |

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

* module [Aspose.Words.Layout](../../)
* class [RevisionOptions](../)

