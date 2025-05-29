---
title: HtmlSaveOptions Class
linktitle: HtmlSaveOptions
articleTitle: HtmlSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.HtmlSaveOptions för att förbättra dokumentsparandet i HTML-, MHTML-, EPUB-, AZW3- och MOBI-format med anpassningsbara alternativ.
type: docs
weight: 5860
url: /sv/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Kan användas för att ange ytterligare alternativ när ett dokument sparas i Html ,Mhtml ,Epub , Azw3 ellerMobi format.

För att lära dig mer, besök[Ange alternativ för sparning](https://docs.aspose.com/words/net/specify-save-options/) dokumentationsartikel.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iHtml format. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iHtml ,Mhtml ,Epub , Azw3 ellerMobi format. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger om inbäddning av teckensnitt med PostScript-konturer ska tillåtas när TrueType-teckensnitt bäddas in i ett dokument när det sparas. Standardvärdet är`falsk` . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | Anger om negativa vänster- och högerindrag i stycken normaliseras när de sparas i HTML, MHTML eller EPUB. Standardvärdet är`falsk` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Anger ett prefix som läggs till alla CSS-klassnamn. Standardvärdet är en tom sträng och genererade CSS-klassnamn har inget gemensamt prefix. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Gör det möjligt att styra hur CSS-stilar sparas när ett dokument sparas i HTML, MHTML eller EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Anger sökvägen och namnet på CSS-filen (Cascading Style Sheet) som skrivs när ett dokument exporteras till HTML. Standardvärdet är en tom sträng. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | Anger hur CSS-stilar (Cascading Style Sheet) exporteras till HTML, MHTML eller EPUB. Standardvärdet ärInline för HTML/MHTML och External för EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Hämtar eller ställer in en anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Hämtar eller anger sökvägen till standardmallen (inklusive filnamn). Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur 3D-effekter renderas. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur DrawingML-former renderas. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Gör det möjligt att styra hur dokumentdelar sparas när ett dokument sparas i HTML eller EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Anger hur dokumentet ska delas upp när det sparas tillHtml , Epub ellerAzw3 format. Standard ärNone för HTML och HeadingParagraph för EPUB och AZW3. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Anger den maximala rubriknivån där dokumentet ska delas. Standardvärdet är`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | Anger vilken kodning som ska användas vid export till HTML, MHTML eller EPUB. Standardvärdet är`ny UTF8-kodning(falsk)` (UTF-8 utan BOM). |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | Anger om CID-URL:er (Content-ID) ska användas för att referera till resurser (bilder, teckensnitt, CSS) som ingår i MHTML -dokument. Standardvärdet är`falsk` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Anger om inbyggda och anpassade dokumentegenskaper ska exporteras till HTML, MHTML eller EPUB. Standardvärdet är`falsk` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Styr hur rullgardinsmenyfält sparas i HTML eller MHTML. Standardvärdet är`falsk` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Anger om teckensnittsresurser ska exporteras till HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Anger om teckensnittsresurser ska bäddas in i HTML i Base64-kodning. Standard är`falsk` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | När`sann` , gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är`sann` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Anger hur sidhuvuden och sidfot visas som HTML, MHTML eller EPUB. Standardvärdet ärPerSection för HTML/MHTML ochNone för EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Anger om bilder sparas i Base64-format som utdata i HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Anger om språkinformation exporteras till HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Styr hur listetiketter matas ut till HTML, MHTML eller EPUB. Standardvärdet ärAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Anger om original-URL:en ska användas som URL för de länkade bilderna. Standardvärdet är`falsk` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Anger om sidmarginaler exporteras till HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Anger om utskriftsformatet exporteras till HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | Anger om teckenstorlekar ska matas ut i relativa enheter när man sparar till HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | Anger om returinformationen ska skrivas när man sparar till HTML, MHTML eller EPUB. Standardvärdet är`sann` för HTML och`falsk` för MHTML och EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | Kontrollerar om[`Shape`](../../aspose.words.drawing/shape/)noder konverteras till SVG-bilder när de sparas till HTML, MHTML, EPUB eller AZW3. Standardvärdet är`falsk` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Styr hur textinmatningsfält sparas i HTML eller MHTML. Standardvärdet är`falsk` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | Anger om sidnummer ska skrivas till innehållsförteckningen när HTML, MHTML och EPUB sparas. Standardvärdet är`falsk` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | Anger om DOCTYPE-deklarationen ska skrivas när man sparar till HTML eller MHTML. När`sann` , skriver en DOCTYPE-deklaration i dokumentet före rotelementet. Standardvärdet är`falsk`. När du sparar till EPUB eller HTML5 (Html5 ) DOCTYPE -deklarationen skrivs alltid. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | Styr vilka teckensnittsresurser som behöver delinställningar när man sparar till HTML, MHTML eller EPUB. Standard är`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Gör det möjligt att styra hur teckensnitt sparas när ett dokument sparas i HTML, MHTML eller EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Anger den fysiska mappen där teckensnitt sparas när ett dokument exporteras till HTML. Standardvärdet är en tom sträng. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Anger namnet på mappen som används för att konstruera teckensnitts-URI:er som skrivs in i ett HTML-dokument. Standardvärdet är en tom sträng. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Anger vilken version av HTML-standarden som ska användas när dokumentet sparas som HTML eller MHTML. Standardvärdet ärXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | Anger utdataupplösningen för bilder vid export till HTML, MHTML eller EPUB. Standard är`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Gör det möjligt att styra hur bilder sparas när ett dokument sparas i HTML, MHTML eller EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Anger den fysiska mappen där bilder sparas när ett dokument exporteras till HTML-format. Standardvärdet är en tom sträng. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Anger namnet på mappen som används för att konstruera bild-URI:er som skrivs in i ett HTML-dokument. Standardvärdet är en tom sträng. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur bläckobjekt (InkML) renderas. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Hämtar eller anger värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är`falsk` . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | Anger i vilket format metafiler sparas vid export till HTML, MHTML eller EPUB. Standardvärdet ärPng , vilket betyder att metafiler renderas till raster-PNG-bilder. |
| [NavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/navigationmaplevel/) { get; set; } | Anger den maximala nivån av rubriker som fylls i navigeringskartan vid export till EPUB-, MOBI- eller AZW3 -format. Standardvärdet är`3` . |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | Styr hur OfficeMath-objekt exporteras till HTML, MHTML eller EPUB. Standardvärdet ärImage . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | När`sann` , pretty formats output där det är tillämpligt. Standardvärdet är`falsk` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Anropas när ett dokument sparas och accepterar data om sparningsförloppet. |
| [RemoveJavaScriptFromLinks](../../aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/) { get; set; } | Anger om JavaScript ska tas bort från länkar. Standard är`falsk` . |
| [ReplaceBackslashWithYenSign](../../aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/) { get; set; } | Anger om bakåtsnedstreck ska ersättas med yen-tecken. Standardvärdet är`falsk` . |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Anger om teckensnittsfamiljenamn som används i dokumentet är upplösta och ersatta enligt [`FontSettings`](../../aspose.words/document/fontsettings/) när det skrivs till HTML-baserade format. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Anger en fysisk mapp där alla resurser som bilder, teckensnitt och extern CSS sparas när ett dokument exporteras till HTML. Standardvärdet är en tom sträng. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Anger namnet på den mapp som används för att konstruera URI:er för alla resurser som skrivs in i ett HTML-dokument. Standardvärdet är en tom sträng. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan varaHtml ,Mhtml ,Epub , Azw3 ellerMobi . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | Anger om bilder skalas av Aspose.Words till den avgränsande formstorleken vid export till HTML, MHTML eller EPUB. Standardvärdet är`sann` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Styr hur tabell-, rad- och cellbredder exporteras till HTML, MHTML eller EPUB. Standardvärdet ärAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Anger mappen för temporära filer som används när man sparar till en DOC- eller DOCX-fil. Som standard är den här egenskapen`null` och inga temporära filer används. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Avgör om teckensnittsattributen ska ändras beroende på den teckenkod som används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan den sparas. Standardvärdet är`falsk` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Hämtar eller anger ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är`sann` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan den sparas. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan den sparas. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Hämtar eller ställer in ett värde som avgör om antialiasing ska användas för rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Hämtar eller ställer in ett värde som avgör om högkvalitativa (dvs. långsamma) renderingsalgoritmer ska användas eller inte. |

## Exempel

Visar hur man anger mappen för att lagra länkade bilder efter att de har sparats till .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Ange ett alternativ för att exportera formulärfält som vanlig text istället för HTML-inmatningselement.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Visar hur man använder en specifik kodning när man sparar ett dokument till .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Som standard kommer ett .epub-dokument att ha allt innehåll i en HTML-del.
// Ett delningskriterium låter oss segmentera dokumentet i flera HTML-delar.
// Vi kommer att ställa in kriterierna för att dela upp dokumentet i rubrikstycken.
// Detta är användbart för läsare som inte kan läsa HTML-filer som är större än en viss storlek.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Ange att vi vill exportera dokumentegenskaper.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Visar hur man delar upp ett dokument i delar och sparar dem.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Skapa ett "HtmlFixedSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
    // för att ändra hur vi konverterar dokumentet till HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Om vi sparar dokumentet normalt kommer det att finnas en HTML-utgång
    // dokument med allt innehåll i källdokumentet.
    // Ställ in egenskapen "DocumentSplitCriteria" till "DocumentSplitCriteria.SectionBreak" till
    // spara vårt dokument till flera HTML-filer: en för varje avsnitt.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Tilldela en anpassad återanropning till egenskapen "DocumentPartSavingCallback" för att ändra logiken för att spara dokumentdelen.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Om vi konverterar ett dokument som innehåller bilder till html, får vi en html-fil som länkar till flera bilder.
    // Varje bild kommer att vara i form av en fil i det lokala filsystemet.
    // Det finns också en återanropsfunktion som kan anpassa namn och filsystemplats för varje bild.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Anger anpassade filnamn för utdatadokument som sparandet delar upp ett dokument i.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // Vi kan komma åt hela källdokumentet via egenskapen "Dokument".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Nedan följer två sätt att ange var Aspose.Words ska spara varje del av dokumentet.
        // 1 - Ange ett filnamn för utdatafilen:
        args.DocumentPartFileName = partFileName;

        // 2 - Skapa en anpassad ström för utdatafilen:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Anger anpassade filnamn för bildfiler som skapas vid en HTML-konvertering.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // Nedan följer två sätt att ange var Aspose.Words ska spara varje del av dokumentet.
        // 1 - Ange ett filnamn för bildfilen som visas:
        args.ImageFileName = imageFileName;

        // 2 - Skapa en anpassad ström för utdatabildfilen:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Se även

* class [SaveOptions](../saveoptions/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
