---
title: RevisionOptions.ShowRevisionBars
linktitle: ShowRevisionBars
second_title: Aspose.Words for .NET API Reference
description: RevisionOptions ShowRevisionBars property. Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is true in C#.
type: docs
weight: 180
url: /net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

Allows to specify whether revision bars should be rendered near lines containing revised content. Default value is `true`.

```csharp
public bool ShowRevisionBars { get; set; }
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

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### See Also

* class [RevisionOptions](../)
* namespace [Aspose.Words.Layout](../../revisionoptions/)
* assembly [Aspose.Words](../../../)
