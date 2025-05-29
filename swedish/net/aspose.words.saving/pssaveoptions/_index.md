---
title: PsSaveOptions Class
linktitle: PsSaveOptions
articleTitle: PsSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.PsSaveOptions för att förbättra din dokumentsparupplevelse i Ps-format med anpassningsbara alternativ för optimala resultat.
type: docs
weight: 6350
url: /sv/net/aspose.words.saving/pssaveoptions/
---
## PsSaveOptions class

Kan användas för att ange ytterligare alternativ när ett dokument sparas iPs format.

För att lära dig mer, besök[Ange alternativ för sparning](https://docs.aspose.com/words/net/specify-save-options/) dokumentationsartikel.

```csharp
public class PsSaveOptions : FixedPageSaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PsSaveOptions](pssaveoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger om inbäddning av teckensnitt med PostScript-konturer ska tillåtas när TrueType-teckensnitt bäddas in i ett dokument när det sparas. Standardvärdet är`falsk` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur färger återges. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Hämtar eller ställer in en anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Hämtar eller anger sökvägen till standardmallen (inklusive filnamn). Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur 3D-effekter renderas. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur DrawingML-former renderas. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | När`sann` , gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är`sann` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur bläckobjekt (InkML) renderas. |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Hämtar eller ställer in ett värde som avgör kvaliteten på JPEG-bilderna i HTML-dokumentet. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Hämtar eller anger värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är`falsk` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Gör det möjligt att ange renderingsalternativ för metafiler. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Hämtar eller sätter[`NumeralFormat`](../numeralformat/) används för rendering av siffror. Europeiska siffror används som standard. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Flaggan anger om det är nödvändigt att optimera utdata. Om denna flagga är inställd tas redundanta kapslade arbetsytor och tomma arbetsytor bort, sammanfogas även angränsande tecken med samma formatering. Obs! Noggrannheten i innehållsvisningen kan påverkas om den här egenskapen är inställd på`sann` . Standard är`falsk` . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Gör det möjligt att styra hur separata sidor sparas när ett dokument exporteras till ett fast sidformat. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Hämtar eller ställer in sidorna som ska renderas. Standard är alla sidor i dokumentet. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | När`sann` , pretty formats output där det är tillämpligt. Standardvärdet är`falsk` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Anropas när ett dokument sparas och accepterar data om sparningsförloppet. |
| override [SaveFormat](../../aspose.words.saving/pssaveoptions/saveformat/) { get; set; } | Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan endast varaPs . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Anger mappen för temporära filer som används när man sparar till en DOC- eller DOCX-fil. Som standard är den här egenskapen`null` och inga temporära filer används. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Avgör om teckensnittsattributen ska ändras beroende på den teckenkod som används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan den sparas. Standardvärdet är`falsk` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Hämtar eller anger ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är`sann` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan den sparas. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan den sparas. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Hämtar eller ställer in ett värde som avgör om antialiasing ska användas för rendering. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/) { get; set; } | Hämtar eller anger ett booleskt värde som anger om dokumentet ska sparas med en layout för broschyrutskrift, om det anges via[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Hämtar eller ställer in ett värde som avgör om högkvalitativa (dvs. långsamma) renderingsalgoritmer ska användas eller inte. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |

## Exempel

Visar hur man sparar ett dokument i Postscript-format i form av en bokvikning.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Skapa ett "PsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till PostScript.
// Sätt egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
// i det utgående Postscript-dokumentet på ett sätt som hjälper oss att skapa ett häfte av det.
// Sätt egenskapen "UseBookFoldPrintingSettings" till "false" för att spara dokumentet normalt.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Om vi renderar dokumentet som ett häfte måste vi ställa in "Flera sidor"
// egenskaper för sidinställningar-objekten för alla sektioner till "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// När vi har skrivit ut det här dokumentet på båda sidor kan vi vika alla sidor på mitten samtidigt,
// och innehållet kommer att radas upp på ett sätt som skapar ett häfte.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Se även

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
