---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words för .NET
description: Aspose.Words.Layout.LayoutOptions klass. Innehåller alternativen som tillåter styrning av dokumentlayoutprocessen i C#.
type: docs
weight: 3350
url: /sv/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

Innehåller alternativen som tillåter styrning av dokumentlayoutprocessen.

För att lära dig mer, besök[Konvertera till fastsidesformat](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) dokumentationsartikel.

```csharp
public class LayoutOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [LayoutOptions](layoutoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | Hämtar eller sätter[`IPageLayoutCallback`](../ipagelayoutcallback/) implementering som används av sidlayoutmodellen. |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | Hämtar eller ställer in hur kommentarer renderas. Standardvärdet ärShowInBalloons . |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | Hämtar eller ställer in beteendet för beräkning av sidnummer när ett kontinuerligt avsnitt startar om sidnumreringen. |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | Hämtar eller ställer in en indikation på om kompatibilitetsalternativet "Använd skrivarmått för att lägga ut dokument" ignoreras. Standard är`Sann` . |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | Hämtar eller ställer in en indikation på huruvida den ursprungliga teckensnittsmåtten ska användas efter teckensnittsersättning. Standard är`Sann` . |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | Får versionsalternativ. |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | Hämtar eller ställer in en indikation på om dold text i dokumentet renderas. Standard är`falsk` . |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | Hämtar eller ställer in en indikation på om stycketecken återges. Standard är`falsk` . |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | Hämtar eller sätter[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/) implementering som används för avancerade typografirenderingsfunktioner. |

## Anmärkningar

Du skapar inte instanser av den här klassen direkt. Använd[`LayoutOptions`](../../aspose.words/document/layoutoptions/) egenskap för att komma åt layoutalternativ för detta dokument.

Observera att efter att ha ändrat något av alternativen som finns i den här klassen,[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) method ska anropas för att de ändrade alternativen ska tillämpas på layouten.

## Exempel

Visar hur man döljer text i ett renderat utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Infoga dold text och ange sedan om vi vill utelämna den från ett renderat dokument.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Visar hur man visar styckemärken i ett renderat utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Lägg till några stycken och aktivera sedan styckemärken för att visa slutet på stycken
// med en pilkråka (¶) symbol när vi renderar dokumentet.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

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
