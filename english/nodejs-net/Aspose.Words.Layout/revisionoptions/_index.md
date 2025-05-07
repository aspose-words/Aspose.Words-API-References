---
title: RevisionOptions class
linktitle: RevisionOptions class
articleTitle: RevisionOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Layout.RevisionOptions class. Allows to control how document revisions are handled during layout process"
type: docs
weight: 110
url: /nodejs-net/aspose.words.layout/revisionoptions/
---

## RevisionOptions class

Allows to control how document revisions are handled during layout process.
To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/nodejs-net/converting-to-fixed-page-format/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [commentColor](./commentColor/) | Allows to specify the color to be used for comments. Default value is [RevisionColor.Red](../revisioncolor/#Red). |
| [deleteCellColor](./deleteCellColor/) | Allows to specify the color to be used for deleted cells [RevisionType.Deletion](../../aspose.words/revisiontype/#Deletion). Default value is [RevisionColor.Pink](../revisioncolor/#Pink). |
| [deletedTextColor](./deletedTextColor/) | Allows to specify the color to be used for deleted content [RevisionType.Deletion](../../aspose.words/revisiontype/#Deletion). Default value is [RevisionColor.ByAuthor](../revisioncolor/#ByAuthor). |
| [deletedTextEffect](./deletedTextEffect/) | Allows to specify the effect to be applied to the deleted content [RevisionType.Deletion](../../aspose.words/revisiontype/#Deletion). Default value is [RevisionTextEffect.StrikeThrough](../revisiontexteffect/#StrikeThrough) |
| [insertCellColor](./insertCellColor/) | Allows to specify the color to be used for inserted cells [RevisionType.Insertion](../../aspose.words/revisiontype/#Insertion). Default value is [RevisionColor.Blue](../revisioncolor/#Blue). |
| [insertedTextColor](./insertedTextColor/) | Allows to specify the color to be used for inserted content [RevisionType.Insertion](../../aspose.words/revisiontype/#Insertion). Default value is [RevisionColor.ByAuthor](../revisioncolor/#ByAuthor). |
| [insertedTextEffect](./insertedTextEffect/) | Allows to specify the effect to be applied to the inserted content [RevisionType.Insertion](../../aspose.words/revisiontype/#Insertion). Default value is [RevisionTextEffect.Underline](../revisiontexteffect/#Underline). |
| [measurementUnit](./measurementUnit/) | Allows to specify the measurement units for revision comments. Default value is [MeasurementUnits.Centimeters](../../aspose.words/measurementunits/#Centimeters) |
| [movedFromTextColor](./movedFromTextColor/) | Allows to specify the color to be used for areas where content was moved from [RevisionType.Moving](../../aspose.words/revisiontype/#Moving). Default value is [RevisionColor.ByAuthor](../revisioncolor/#ByAuthor). |
| [movedFromTextEffect](./movedFromTextEffect/) | Allows to specify the effect to be applied to the areas where content was moved from [RevisionType.Moving](../../aspose.words/revisiontype/#Moving). Default value is [RevisionTextEffect.DoubleStrikeThrough](../revisiontexteffect/#DoubleStrikeThrough) |
| [movedToTextColor](./movedToTextColor/) | Allows to specify the color to be used for areas where content was moved to [RevisionType.Moving](../../aspose.words/revisiontype/#Moving). Default value is [RevisionColor.ByAuthor](../revisioncolor/#ByAuthor). |
| [movedToTextEffect](./movedToTextEffect/) | Allows to specify the effect to be applied to the areas where content was moved to [RevisionType.Moving](../../aspose.words/revisiontype/#Moving). Default value is [RevisionTextEffect.DoubleUnderline](../revisiontexteffect/#DoubleUnderline) |
| [revisedPropertiesColor](./revisedPropertiesColor/) | Allows to specify the color to be used for content with changes of formatting properties [RevisionType.FormatChange](../../aspose.words/revisiontype/#FormatChange) Default value is [RevisionColor.NoHighlight](../revisioncolor/#NoHighlight). |
| [revisedPropertiesEffect](./revisedPropertiesEffect/) | Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FormatChange](../../aspose.words/revisiontype/#FormatChange) Default value is [RevisionTextEffect.None](../revisiontexteffect/#None) |
| [revisionBarsColor](./revisionBarsColor/) | Allows to specify the color to be used for side bars that identify document lines containing revised information. Default value is [RevisionColor.Red](../revisioncolor/#Red). |
| [revisionBarsPosition](./revisionBarsPosition/) | Gets or sets rendering position of revision bars. Default value is [HorizontalAlignment.Outside](../../aspose.words.drawing/horizontalalignment/#Outside). |
| [revisionBarsWidth](./revisionBarsWidth/) | Gets or sets width of revision bars, points. |
| [showInBalloons](./showInBalloons/) | Allows to specify whether the revisions are rendered in the balloons. Default value is [ShowInBalloons.None](../showinballoons/#None). |
| [showOriginalRevision](./showOriginalRevision/) | Allows to specify whether the original text should be shown instead of revised one. Default value is ``false``. |
| [showRevisionBars](./showRevisionBars/) | Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is ``true``. |
| [showRevisionMarks](./showRevisionMarks/) | Allow to specify whether revision text should be marked with special formatting markup. Default value is ``true``. |

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

* module [Aspose.Words.Layout](../)

