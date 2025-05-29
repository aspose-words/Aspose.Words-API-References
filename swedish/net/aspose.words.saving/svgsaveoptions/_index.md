---
title: SvgSaveOptions Class
linktitle: SvgSaveOptions
articleTitle: SvgSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.SvgSaveOptions för att förbättra din dokumentkonvertering till SVG-format med anpassningsbara funktioner för optimala resultat.
type: docs
weight: 6400
url: /sv/net/aspose.words.saving/svgsaveoptions/
---
## SvgSaveOptions class

Kan användas för att ange ytterligare alternativ när ett dokument sparas iSvg format.

För att lära dig mer, besök[Ange alternativ för sparning](https://docs.aspose.com/words/net/specify-save-options/) dokumentationsartikel.

```csharp
public class SvgSaveOptions : FixedPageSaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [SvgSaveOptions](svgsaveoptions/)() | Default_Constructor |

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
| [ExportEmbeddedImages](../../aspose.words.saving/svgsaveoptions/exportembeddedimages/) { get; set; } | Anger om bilder ska bäddas in i SVG-dokumentet som base64. Tänk på att aktivering av det här alternativet kan leda till en betydande ökning av storleken på den utgående SVG-filen. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | När`sann` , gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är`sann` . |
| [FitToViewPort](../../aspose.words.saving/svgsaveoptions/fittoviewport/) { get; set; } | Anger om utdata-SVG-filen ska fylla det tillgängliga visningsområdet (webbläsarfönster eller container). När den är inställd på`sann`Bredd och höjd på utdata-SVG är inställda på 100 %. |
| [IdPrefix](../../aspose.words.saving/svgsaveoptions/idprefix/) { get; set; } | Anger ett prefix som läggs till före alla genererade element-ID:n i utdatadokumentet. Standardvärdet är null och inget prefix läggs till. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur bläckobjekt (InkML) renderas. |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Hämtar eller ställer in ett värde som avgör kvaliteten på JPEG-bilderna i HTML-dokumentet. |
| [MaxImageResolution](../../aspose.words.saving/svgsaveoptions/maximageresolution/) { get; set; } | Hämtar eller ställer in ett värde i pixlar per tum som begränsar upplösningen för exporterade rasterbilder. Standardvärdet är noll. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Hämtar eller anger värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är`falsk` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Gör det möjligt att ange renderingsalternativ för metafiler. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Hämtar eller sätter[`NumeralFormat`](../numeralformat/) används för rendering av siffror. Europeiska siffror används som standard. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Flaggan anger om det är nödvändigt att optimera utdata. Om denna flagga är inställd tas redundanta kapslade arbetsytor och tomma arbetsytor bort, sammanfogas även angränsande tecken med samma formatering. Obs! Noggrannheten i innehållsvisningen kan påverkas om den här egenskapen är inställd på`sann` . Standard är`falsk` . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Gör det möjligt att styra hur separata sidor sparas när ett dokument exporteras till ett fast sidformat. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Hämtar eller ställer in sidorna som ska renderas. Standard är alla sidor i dokumentet. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | När`sann` , pretty formats output där det är tillämpligt. Standardvärdet är`falsk` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Anropas när ett dokument sparas och accepterar data om sparningsförloppet. |
| [RemoveJavaScriptFromLinks](../../aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/) { get; set; } | Anger om JavaScript ska tas bort från länkar. Standard är`falsk` . Om det här alternativet är aktiverat kommer alla länkar som innehåller JavaScript att ersättas med "javascript:void(0)". |
| [ResourceSavingCallback](../../aspose.words.saving/svgsaveoptions/resourcesavingcallback/) { get; set; } | Gör det möjligt att styra hur resurser (bilder) sparas när ett dokument exporteras till SVG-format. |
| [ResourcesFolder](../../aspose.words.saving/svgsaveoptions/resourcesfolder/) { get; set; } | Anger den fysiska mappen där resurser (bilder) sparas när ett dokument exporteras till Svg-format. Standard är`null` . |
| [ResourcesFolderAlias](../../aspose.words.saving/svgsaveoptions/resourcesfolderalias/) { get; set; } | Anger namnet på mappen som används för att konstruera bild-URI:er som skrivs in i ett SVG-dokument. Standard är`null` . |
| override [SaveFormat](../../aspose.words.saving/svgsaveoptions/saveformat/) { get; set; } | Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan endast varaSvg . |
| [ShowPageBorder](../../aspose.words.saving/svgsaveoptions/showpageborder/) { get; set; } | Styr om en kantlinje läggs till i sidans kontur. Standard är`sann` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Anger mappen för temporära filer som används när man sparar till en DOC- eller DOCX-fil. Som standard är den här egenskapen`null` och inga temporära filer används. |
| [TextOutputMode](../../aspose.words.saving/svgsaveoptions/textoutputmode/) { get; set; } | Hämtar eller anger ett värde som avgör hur text ska renderas i SVG. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Avgör om teckensnittsattributen ska ändras beroende på den teckenkod som används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan den sparas. Standardvärdet är`falsk` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Hämtar eller anger ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är`sann` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan den sparas. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan den sparas. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Hämtar eller ställer in ett värde som avgör om antialiasing ska användas för rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Hämtar eller ställer in ett värde som avgör om högkvalitativa (dvs. långsamma) renderingsalgoritmer ska användas eller inte. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |

## Exempel

Visar hur man manipulerar och skriver ut URI:er för länkade resurser som skapats vid konvertering av ett dokument till .svg.

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// Räknar och skriver ut URI:er för resurser som finns i formatet allt eftersom de konverteras till .svg.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### Se även

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
