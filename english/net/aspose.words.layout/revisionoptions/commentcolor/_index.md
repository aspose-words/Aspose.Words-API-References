---
title: RevisionOptions.CommentColor
linktitle: CommentColor
articleTitle: CommentColor
second_title: Aspose.Words for .NET
description: Customize your comments with RevisionOptions' CommentColor property. Easily set your preferred color—default is red—for enhanced visibility!
type: docs
weight: 10
url: /net/aspose.words.layout/revisionoptions/commentcolor/
---
## RevisionOptions.CommentColor property

Allows to specify the color to be used for comments. Default value is Red.

```csharp
public RevisionColor CommentColor { get; set; }
```

## Remarks

If this property is set to NoHighlight, the default color will be used for comments.

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

Shows how to render comments of each author in a different color.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Comment from John.");
builder.CurrentParagraph.AppendChild(comment);

builder.Writeln();
builder.Write("Hello again!");
comment = new Comment(doc, "Jane Doe", "J.D.", DateTime.Now);
comment.SetText("Comment from Jane.");
builder.CurrentParagraph.AppendChild(comment);

// Similar to Microsoft Word, the "ByAuthor" color affects regular comments as well as revision comments.
// Comment balloons of different authors are rendered in different colors.
doc.LayoutOptions.RevisionOptions.CommentColor = RevisionColor.ByAuthor;

// This option is only applicable to formats such as .pdf or .jpg.
doc.Save(ArtifactsDir + "Revision.CommentColorByAuthor.pdf");
```

### See Also

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* namespace [Aspose.Words.Layout](../../../aspose.words.layout/)
* assembly [Aspose.Words](../../../)
