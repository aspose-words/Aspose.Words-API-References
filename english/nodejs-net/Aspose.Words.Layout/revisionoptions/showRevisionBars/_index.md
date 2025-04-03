---
title: RevisionOptions.showRevisionBars property
linktitle: showRevisionBars property
articleTitle: showRevisionBars property
second_title: Aspose.Words for NodeJs
description: "RevisionOptions.showRevisionBars property. Allows to specify whether revision bars should be rendered near lines containing revised content"
type: docs
weight: 200
url: /nodejs-net/Aspose.Words.Layout/revisionoptions/showRevisionBars/
---

## RevisionOptions.showRevisionBars property

Allows to specify whether revision bars should be rendered near lines containing revised content.
Default value is ``true``.



```js
get showRevisionBars(): boolean
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

