---
title: Class RevisionOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Layout.RevisionOptions klass. Gör det möjligt att styra hur dokumentrevisioner hanteras under layoutprocessen.
type: docs
weight: 3390
url: /sv/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Gör det möjligt att styra hur dokumentrevisioner hanteras under layoutprocessen.

För att lära dig mer, besök[Konvertera till fastsidesformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokumentationsartikel.

```csharp
public class RevisionOptions
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för kommentarer. Standardvärdet ärRed . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Tillåter att ange färgen som ska användas för borttaget innehållDeletion . Standardvärdet ärByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Tillåter att specificera effekten som ska tillämpas på det raderade innehålletDeletion . Standardvärdet ärStrikeThrough |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Tillåter att ange färgen som ska användas för infogat innehållInsertion . Standardvärdet ärByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Tillåter att specificera effekten som ska tillämpas på det infogade innehålletInsertion . Standardvärdet ärUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Gör det möjligt att ange måttenheter för revisionskommentarer. Standardvärdet ärCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Tillåter att ange färgen som ska användas för områden där innehållet har flyttats frånMoving . Standardvärdet ärByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Tillåter att specificera effekten som ska tillämpas på de områden där innehållet flyttades frånMoving . Standardvärdet ärDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Tillåter att ange färgen som ska användas för områden där innehållet har flyttats tillMoving . Standardvärdet ärByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Tillåter att ange effekten som ska tillämpas på de områden där innehållet flyttades tillMoving . Standardvärdet ärDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Tillåter att ange färgen som ska användas för innehåll med ändringar av formateringsegenskaperFormatChange Standardvärdet ärNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Tillåter att specificera effekten för innehållsområden med ändringar av formateringsegenskaperFormatChange Standardvärdet ärNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för sidofält som identifierar dokumentrader som innehåller reviderad information. Standardvärdet ärRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Hämtar eller ställer in renderingsposition för revisionsstaplar. Standardvärdet ärOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Hämtar eller ställer in bredden på revisionsstaplar, punkter. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Gör det möjligt att ange om revisionerna ska återges i ballongerna. Standardvärdet ärNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Tillåter att ange om den ursprungliga texten ska visas istället för en reviderad. Standardvärdet är`falsk` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Tillåter att ange om revisionsstaplar ska renderas nära linjer som innehåller reviderat innehåll. Standardvärdet är`Sann` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Tillåt att ange om versionstext ska markeras med speciell formateringsmarkering. Standardvärdet är`Sann` . |

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

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)


