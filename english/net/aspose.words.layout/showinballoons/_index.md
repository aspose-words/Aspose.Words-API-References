---
title: ShowInBalloons Enum
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Layout.ShowInBalloons enum. Specifies which revisions are rendered in balloons in C#.
type: docs
weight: 3230
url: /net/aspose.words.layout/showinballoons/
---
## ShowInBalloons enumeration

Specifies which revisions are rendered in balloons.

```csharp
public enum ShowInBalloons
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Renders insert, delete and format revisions inline. |
| Format | `1` | Renders insert and delete revisions inline, format revisions in balloons. |
| FormatAndDelete | `2` | Renders insert revisions inline, delete and format revisions in balloons. |

## Remarks

Note that revisions are not rendered in balloons for ShowInAnnotations.

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
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

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

* namespace [Aspose.Words.Layout](../../aspose.words.layout/)
* assembly [Aspose.Words](../../)
