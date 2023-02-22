---
title: LayoutOptions.RevisionOptions
second_title: Aspose.Words för .NET API Referens
description: LayoutOptions fast egendom. Får versionsalternativ.
type: docs
weight: 60
url: /sv/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

Får versionsalternativ.

```csharp
public RevisionOptions RevisionOptions { get; }
```

### Exempel

Visar hur man ändrar utseendet på revisioner i ett renderat utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en revision och ändra sedan färgen på alla versioner till grön.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Ta bort stapeln som visas till vänster om varje reviderad rad.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Se även

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../layoutoptions/)
* hopsättning [Aspose.Words](../../../)


