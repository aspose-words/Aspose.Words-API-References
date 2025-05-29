---
title: LayoutOptions.RevisionOptions
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words för .NET
description: Utforska egenskapen LayoutOptions RevisionOptions för att enkelt komma åt och anpassa revisionsinställningar för förbättrad dokumentkontroll och flexibilitet.
type: docs
weight: 70
url: /sv/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

Hämtar revisionsalternativ.

```csharp
public RevisionOptions RevisionOptions { get; }
```

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

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
