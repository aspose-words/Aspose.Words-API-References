---
title: RevisionOptions.InsertedTextColor
linktitle: InsertedTextColor
articleTitle: InsertedTextColor
second_title: Aspose.Words for .NET
description: Customize your editing experience with the RevisionOptions InsertedTextColor property, setting unique colors for inserted content. Default, ByAuthor.
type: docs
weight: 60
url: /net/aspose.words.layout/revisionoptions/insertedtextcolor/
---
## RevisionOptions.InsertedTextColor property

Allows to specify the color to be used for inserted content Insertion. Default value is ByAuthor.

```csharp
public RevisionColor InsertedTextColor { get; set; }
```

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

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* namespace [Aspose.Words.Layout](../../../aspose.words.layout/)
* assembly [Aspose.Words](../../../)
