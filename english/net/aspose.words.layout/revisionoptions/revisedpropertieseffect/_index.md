---
title: RevisionOptions.RevisedPropertiesEffect
linktitle: RevisedPropertiesEffect
articleTitle: RevisedPropertiesEffect
second_title: Aspose.Words for .NET
description: Discover how the RevisedPropertiesEffect in RevisionOptions enhances your content formatting. Easily customize changes with the FormatChange feature.
type: docs
weight: 140
url: /net/aspose.words.layout/revisionoptions/revisedpropertieseffect/
---
## RevisionOptions.RevisedPropertiesEffect property

Allows to specify the effect for content areas with changes of formatting properties FormatChange Default value is None

```csharp
public RevisionTextEffect RevisedPropertiesEffect { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Hidden is not allowed. |

## Examples

Shows how to modify the appearance of revisions.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Get the RevisionOptions object that controls the appearance of revisions.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Render insertion revisions in green and italic.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Render deletion revisions in red and bold.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// The same text will appear twice in a movement revision:
// once at the departure point and once at the arrival destination.
// Render the text at the moved-from revision yellow with a double strike through
// and double-underlined blue at the moved-to revision.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedToTextEffect = RevisionTextEffect.DoubleUnderline;

// Render format revisions in dark red and bold.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Show revision marks and original text.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Get movement, deletion, formatting revisions, and comments to show up in green balloons
// on the right side of the page.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// These features are only applicable to formats such as .pdf or .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### See Also

* enum [RevisionTextEffect](../../revisiontexteffect/)
* class [RevisionOptions](../)
* namespace [Aspose.Words.Layout](../../../aspose.words.layout/)
* assembly [Aspose.Words](../../../)
