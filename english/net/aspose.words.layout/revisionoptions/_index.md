---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Layout.RevisionOptions class to efficiently manage document revisions and enhance your layout process for optimal results.
type: docs
weight: 3850
url: /net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Allows to control how document revisions are handled during layout process.

To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) documentation article.

```csharp
public class RevisionOptions
```

## Properties

| Name | Description |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Allows to specify the color to be used for comments. Default value is Red. |
| [DeleteCellColor](../../aspose.words.layout/revisionoptions/deletecellcolor/) { get; set; } | Allows to specify the color to be used for deleted cells Deletion. Default value is Pink. |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Allows to specify the color to be used for deleted content Deletion. Default value is ByAuthor. |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Allows to specify the effect to be applied to the deleted content Deletion. Default value is StrikeThrough |
| [InsertCellColor](../../aspose.words.layout/revisionoptions/insertcellcolor/) { get; set; } | Allows to specify the color to be used for inserted cells Insertion. Default value is Blue. |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Allows to specify the color to be used for inserted content Insertion. Default value is ByAuthor. |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Allows to specify the effect to be applied to the inserted content Insertion. Default value is Underline. |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Allows to specify the measurement units for revision comments. Default value is Centimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Allows to specify the color to be used for areas where content was moved from Moving. Default value is ByAuthor. |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Allows to specify the effect to be applied to the areas where content was moved from Moving. Default value is DoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Allows to specify the color to be used for areas where content was moved to Moving. Default value is ByAuthor. |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Allows to specify the effect to be applied to the areas where content was moved to Moving. Default value is DoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Allows to specify the color to be used for content with changes of formatting properties FormatChange Default value is NoHighlight. |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Allows to specify the effect for content areas with changes of formatting properties FormatChange Default value is None |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Allows to specify the color to be used for side bars that identify document lines containing revised information. Default value is Red. |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Gets or sets rendering position of revision bars. Default value is Outside. |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Gets or sets width of revision bars, points. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Allows to specify whether the revisions are rendered in the balloons. Default value is None. |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Allows to specify whether the original text should be shown instead of revised one. Default value is `false`. |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is `true`. |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Allow to specify whether revision text should be marked with special formatting markup. Default value is `true`. |

## Examples

Shows how to alter the appearance of revisions in a rendered output document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a revision, then change the color of all revisions to green.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Remove the bar that appears to the left of every revised line.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### See Also

* namespace [Aspose.Words.Layout](../../aspose.words.layout/)
* assembly [Aspose.Words](../../)
