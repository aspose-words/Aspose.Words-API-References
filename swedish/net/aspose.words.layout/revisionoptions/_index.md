---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Layout.RevisionOptions för att effektivt hantera dokumentrevisioner och förbättra din layoutprocess för optimala resultat.
type: docs
weight: 3840
url: /sv/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Gör det möjligt att styra hur dokumentrevisioner hanteras under layoutprocessen.

För att lära dig mer, besök[Konvertera till fast sidformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokumentationsartikel.

```csharp
public class RevisionOptions
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för kommentarer. Standardvärdet ärRed . |
| [DeleteCellColor](../../aspose.words.layout/revisionoptions/deletecellcolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för borttagna cellerDeletion . Standardvärdet ärPink . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för borttaget innehållDeletion . Standardvärdet ärByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Gör det möjligt att ange vilken effekt som ska tillämpas på det borttagna innehålletDeletion . Standardvärdet ärStrikeThrough |
| [InsertCellColor](../../aspose.words.layout/revisionoptions/insertcellcolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för infogade cellerInsertion . Standardvärdet ärBlue . |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för infogat innehållInsertion . Standardvärdet ärByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Gör det möjligt att ange vilken effekt som ska tillämpas på det infogade innehålletInsertion . Standardvärdet ärUnderline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Gör det möjligt att ange måttenheter för revisionskommentarer. Standardvärdet ärCentimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för områden där innehåll flyttades frånMoving . Standardvärdet ärByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Gör det möjligt att ange effekten som ska tillämpas på de områden där innehåll flyttades frånMoving . Standardvärdet ärDoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för områden dit innehåll flyttadesMoving . Standardvärdet ärByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Gör det möjligt att ange effekten som ska tillämpas på de områden dit innehåll flyttadesMoving . Standardvärdet ärDoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för innehåll med ändringar i formateringsegenskaper.FormatChange Standardvärdet ärNoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Gör det möjligt att ange effekten för innehållsområden med ändringar av formateringsegenskaperFormatChange Standardvärdet ärNone |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Gör det möjligt att ange färgen som ska användas för sidofält som identifierar dokumentrader som innehåller reviderad information. Standardvärdet ärRed . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Hämtar eller ställer in renderingspositionen för revisionsstaplarna. Standardvärdet ärOutside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Hämtar eller ställer in bredden på revisionsstaplar och punkter. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Gör det möjligt att ange om revisionerna ska renderas i ballongerna. Standardvärdet ärNone . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Gör det möjligt att ange om originaltexten ska visas istället för den reviderade. Standardvärdet är`falsk` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Gör det möjligt att ange om revisionsfält ska visas nära rader som innehåller reviderat innehåll. Standardvärdet är`sann` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Tillåter att ange om revisionstext ska markeras med speciell formateringsmarkering. Standardvärdet är`sann` . |

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

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
