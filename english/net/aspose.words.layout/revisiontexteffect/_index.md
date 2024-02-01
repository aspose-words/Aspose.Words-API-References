---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words for .NET
description: Aspose.Words.Layout.RevisionTextEffect enum. Allows to specify decoration effect for revisions of document text in C#.
type: docs
weight: 3530
url: /net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

Allows to specify decoration effect for revisions of document text.

```csharp
public enum RevisionTextEffect
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Revised content has no special effects applied. This corresponds to NoHighlight. |
| Color | `1` | Revised content is highlighted with color only. |
| Bold | `2` | Revised content is made bold and colored. |
| Italic | `3` | Revised content is made italic and colored. |
| Underline | `4` | Revised content is underlined and colored. |
| DoubleUnderline | `5` | Revised content is double underlined and colored. |
| StrikeThrough | `6` | Revised content is stroked through and colored. |
| DoubleStrikeThrough | `7` | Revised content is double stroked through and colored. |
| Hidden | `8` | Revised content is hidden. |

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
