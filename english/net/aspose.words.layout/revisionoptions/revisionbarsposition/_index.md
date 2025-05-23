---
title: RevisionOptions.RevisionBarsPosition
linktitle: RevisionBarsPosition
articleTitle: RevisionBarsPosition
second_title: Aspose.Words for .NET
description: Discover how to customize the RevisionBarsPosition property in RevisionOptions to enhance your document's appearance. Default is set to Outside.
type: docs
weight: 160
url: /net/aspose.words.layout/revisionoptions/revisionbarsposition/
---
## RevisionOptions.RevisionBarsPosition property

Gets or sets rendering position of revision bars. Default value is Outside.

```csharp
public HorizontalAlignment RevisionBarsPosition { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Values of Center and Inside are not allowed. |

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

* enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* class [RevisionOptions](../)
* namespace [Aspose.Words.Layout](../../../aspose.words.layout/)
* assembly [Aspose.Words](../../../)
