---
title: RevisionColor enumeration
linktitle: RevisionColor enumeration
articleTitle: RevisionColor enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Layout.RevisionColor enumeration. Allows to specify color of document revisions."
type: docs
weight: 100
url: /nodejs-net/aspose.words.layout/revisioncolor/
---

## RevisionColor enumeration

Allows to specify color of document revisions.


### Members

| Name | Description |
| --- | --- |
| Auto | Default. |
| Black | Represents 000000 color. |
| Blue | Represents 2e97d3 color. |
| BrightGreen | Represents 84a35b color. |
| ClassicBlue | Represents 0000ff color. |
| ClassicRed | Represents ff0000 color. |
| DarkBlue | Represents 376e96 color. |
| DarkRed | Represents 881824 color. |
| DarkYellow | Represents e09a2b color. |
| Gray25 | Represents a0a3a9 color. |
| Gray50 | Represents 50565e color. |
| Green | Represents 2c6234 color. |
| Pink | Represents ce338f color. |
| Red | Represents b5082e color. |
| Teal | Represents 1b9cab color. |
| Turquoise | Represents 3eafc2 color. |
| Violet | Represents 633277 color. |
| White | Represents ffffff color. |
| Yellow | Represents fad272 color. |
| LightPink | Represents fce6f4 color. |
| LightBlue | Represents e1f2fa color. |
| LightYellow | Represents fef4de color. |
| LightPurple | Represents eadfef color. |
| LightOrange | Represents fce3d0 color. |
| LightGreen | Represents e9f8ce color. |
| Gray | Represents efeded color. |
| NoHighlight | No color is used to highlight revision changes. |
| ByAuthor | Revisions of each author receive their own color for highlighting from a predefined set of hi-contrast colors. |

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

* module [Aspose.Words.Layout](../)

