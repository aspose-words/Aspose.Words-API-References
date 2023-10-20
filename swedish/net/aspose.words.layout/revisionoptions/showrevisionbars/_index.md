---
title: RevisionOptions.ShowRevisionBars
linktitle: ShowRevisionBars
articleTitle: ShowRevisionBars
second_title: Aspose.Words för .NET
description: RevisionOptions ShowRevisionBars fast egendom. Tillåter att ange om revisionsstaplar ska renderas nära linjer som innehåller reviderat innehåll. Standardvärdet ärSann  i C#.
type: docs
weight: 180
url: /sv/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

Tillåter att ange om revisionsstaplar ska renderas nära linjer som innehåller reviderat innehåll. Standardvärdet är`Sann` .

```csharp
public bool ShowRevisionBars { get; set; }
```

## Exempel

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

* class [RevisionOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
