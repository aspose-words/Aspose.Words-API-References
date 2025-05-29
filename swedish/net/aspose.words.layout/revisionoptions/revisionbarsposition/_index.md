---
title: RevisionOptions.RevisionBarsPosition
linktitle: RevisionBarsPosition
articleTitle: RevisionBarsPosition
second_title: Aspose.Words för .NET
description: Upptäck hur du anpassar egenskapen RevisionBarsPosition i RevisionOptions för att förbättra dokumentets utseende. Standardinställningen är Utanför.
type: docs
weight: 160
url: /sv/net/aspose.words.layout/revisionoptions/revisionbarsposition/
---
## RevisionOptions.RevisionBarsPosition property

Hämtar eller ställer in renderingspositionen för revisionsstaplarna. Standardvärdet ärOutside .

```csharp
public HorizontalAlignment RevisionBarsPosition { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentOutOfRangeException | Värden avCenter ochInside är inte tillåtna. |

## Exempel

Visar hur man ändrar utseendet på revisioner i ett renderat utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en revision och ändra sedan färgen på alla revisioner till grön.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Ta bort fältet som visas till vänster om varje reviderad rad.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Se även

* enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* class [RevisionOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
