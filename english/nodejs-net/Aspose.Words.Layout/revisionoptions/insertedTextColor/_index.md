---
title: RevisionOptions.insertedTextColor property
linktitle: insertedTextColor property
articleTitle: insertedTextColor property
second_title: Aspose.Words for NodeJs
description: "RevisionOptions.insertedTextColor property. Allows to specify the color to be used for inserted content [RevisionType.Insertion](../../../Aspose.Words/revisiontype/#Insertion)"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Layout/revisionoptions/insertedTextColor/
---

## RevisionOptions.insertedTextColor property

Allows to specify the color to be used for inserted content [RevisionType.Insertion](../../../Aspose.Words/revisiontype/#Insertion).
Default value is [RevisionColor.ByAuthor](../../revisioncolor/#ByAuthor).



```js
get insertedTextColor(): Aspose.Words.Layout.RevisionColor
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

doc.save(base.artifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### See Also

* module [Aspose.Words.Layout](../../)
* class [RevisionOptions](../)

