---
title: Class HtmlSaveOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.HtmlSaveOptions klass. Kan användas för att ange ytterligare alternativ när du sparar ett dokument iHtml  Mhtml ellerEpub format.
type: docs
weight: 4850
url: /sv/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Kan användas för att ange ytterligare alternativ när du sparar ett dokument iHtml , Mhtml ellerEpub format.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Initierar en ny instans av denna klass som kan användas för att spara ett document iHtml format. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(SaveFormat) | Initierar en ny instans av denna klass som kan användas för att spara ett document iHtml ,Mhtml ellerEpub format. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar om man ska tillåta inbäddning av teckensnitt med PostScript outlines när inbäddning av TrueType-teckensnitt i ett dokument på det sparas. Standardvärdet är **falsk** . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | Anger om negativa vänster- och högerindrag i stycken normaliseras när du sparar till HTML, MHTML eller EPUB. Standardvärdet är`falsk` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Anger ett prefix som läggs till i alla CSS-klassnamn. Standardvärdet är en tom sträng och genererade CSS-klassnamn har inget gemensamt prefix. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Gör det möjligt att styra hur CSS-stilar sparas när ett dokument sparas i HTML, MHTML eller EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Anger sökvägen och namnet på CSS-filen (Cascading Style Sheet) som skrivs när ett document exporteras till HTML. Standard är en tom sträng. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | Anger hur CSS-stilar (Cascading Style Sheet) exporteras till HTML, MHTML eller EPUB. Standardvärdet ärInline för HTML/MHTML och External för EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Hämtar eller ställer in anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Hämtar eller ställer in sökvägen till standardmall (inklusive filnamn). Standardvärdet för den här egenskapen är **tom sträng** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur 3D-effekter renderas. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-former renderas. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Gör det möjligt att styra hur dokumentdelar sparas när ett dokument sparas i HTML eller EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Anger hur dokumentet ska delas när du sparar tillHtml ellerEpub formatera. Standard ärNone för HTML och HeadingParagraph för EPUB. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Anger den maximala nivån för rubriker för att dela dokumentet. Standardvärdet är`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | Anger kodningen som ska användas vid export till HTML, MHTML eller EPUB. Standardvärdet är`ny UTF8Encoding(false)` (UTF-8 utan stycklista). |
| [EpubNavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/) { get; set; } | Anger den maximala nivån för rubriker som fylls i navigationskartan vid export till IDPF EPUB-format. Standardvärdet är`3` . |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | Anger om CID-webbadresser (Content-ID) ska användas för att referera till resurser (bilder, teckensnitt, CSS) som ingår i MHTML -dokument. Standardvärdet är`falsk` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Anger om inbyggda och anpassade dokumentegenskaper ska exporteras till HTML, MHTML eller EPUB. Standardvärdet är`falsk` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Styr hur formulärfält i rullgardinsmenyn sparas i HTML eller MHTML. Standardvärdet är`falsk` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Anger om teckensnittsresurser ska exporteras till HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Anger om teckensnittsresurser ska bäddas in i HTML i Base64-kodning. Standard är`falsk` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | När sant, gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är **Sann** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Anger hur sidhuvuden och sidfötter matas ut till HTML, MHTML eller EPUB. Standardvärdet ärPerSection för HTML/MHTML ochNone för EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Anger om bilder sparas i Base64-format till utdata HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Anger om språkinformation exporteras till HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Styr hur listetiketter matas ut till HTML, MHTML eller EPUB. Standardvärdet ärAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Anger om den ursprungliga webbadressen ska användas som URL för de länkade bilderna. Standardvärdet är`falsk` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Anger om sidmarginaler exporteras till HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Anger om sidinställningarna exporteras till HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | Anger om teckenstorlekar ska matas ut i relativa enheter när du sparar till HTML, MHTML eller EPUB. Standard är`falsk` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | Anger om informationen tur och retur ska skrivas när du sparar till HTML, MHTML eller EPUB. Standardvärdet är`Sann` för HTML och`falsk` för MHTML och EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | Styr om[`Shape`](../../aspose.words.drawing/shape/) noder konverteras till SVG-bilder när du sparar till HTML, MHTML eller EPUB. Standardvärdet är`falsk` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Styr hur formulärfält för textinmatning sparas i HTML eller MHTML. Standardvärdet är`falsk` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | Anger om sidnummer ska skrivas till innehållsförteckningen när HTML, MHTML och EPUB sparas. Standardvärdet är`falsk` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | Anger om DOCTYPE-deklarationen ska skrivas när du sparar till HTML eller MHTML. När`Sann` , skriver en DOCTYPE-deklaration i dokumentet före rotelementet. Standardvärdet är`falsk`. När du sparar till EPUB eller HTML5 (Html5 ) DOCTYPE -deklarationen skrivs alltid. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas av[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Endast som standardFlatOpc dokumentformat får mappas. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | Styr vilka teckensnittsresurser som behöver underinställning när du sparar till HTML, MHTML eller EPUB. Standard är`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Gör det möjligt att styra hur teckensnitt sparas när ett dokument sparas i HTML, MHTML eller EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Anger den fysiska mapp där teckensnitt sparas vid export av ett dokument till HTML. Standard är en tom sträng. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Anger namnet på mappen som används för att konstruera teckensnitts-URI:er inskrivna i ett HTML-dokument. Standard är en tom sträng. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Anger version av HTML-standarden som ska användas när dokumentet sparas till HTML eller MHTML. Standardvärdet ärXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | Anger utdataupplösningen för bilder vid export till HTML, MHTML eller EPUB. Standard är`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Gör det möjligt att styra hur bilder sparas när ett dokument sparas i HTML, MHTML eller EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Anger den fysiska mappen där bilder sparas vid export av ett dokument till HTML-format. Standard är en tom sträng. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Anger namnet på mappen som används för att konstruera bild-URI:er inskrivna i ett HTML-dokument. Standard är en tom sträng. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur bläckobjekt (InkML) renderas. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Hämtar eller ställer in värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är **falsk** . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | Anger i vilket format metafiler sparas vid export till HTML, MHTML eller EPUB. Standardvärdet ärPng , vilket betyder att metafiler renderas till raster PNG-bilder. |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | Styr hur OfficeMath-objekt exporteras till HTML, MHTML eller EPUB. Standardvärdet är`HtmlOfficeMathOutputMode.Image` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | När`Sann` , snygga format utdata där tillämpligt. Standardvärdet är **falsk** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Anropas när ett dokument sparas och accepterar data om lagringsförlopp. |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Anger om teckensnittsfamiljnamn som används i dokumentet löses och ersätts enligt [`FontSettings`](../../aspose.words/document/fontsettings/) när de skrivs i HTML-baserade format. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Anger en fysisk mapp där alla resurser som bilder, typsnitt och extern CSS sparas när ett document exporteras till HTML. Standard är en tom sträng. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Anger namnet på mappen som används för att konstruera URI:er för alla resurser som skrivits in i ett HTML-dokument. Standard är en tom sträng. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Anger formatet som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan varaHtml ,Mhtml ellerEpub . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | Anger om bilder skalas av Aspose.Words till den gränsande formstorleken vid export till HTML, MHTML eller EPUB. Standardvärdet är`Sann` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Styr hur tabell-, rad- och cellbredder exporteras till HTML, MHTML eller EPUB. Standardvärdet ärAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Anger mappen för temporära filer som används när du sparar till en DOC- eller DOCX-fil. Som standard är denna egenskap`null` och inga temporära filer används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan du sparar. Standardvärdet är falskt; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Hämtar eller ställer in ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är **Sann** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan du sparar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan du sparar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Hämtar eller ställer in värde som avgör om innehållet i[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) uppdateras innan du sparar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Hämtar eller ställer in ett värde som avgör om kantutjämning ska användas eller inte för rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Hämtar eller ställer in ett värde som avgör huruvida högkvalitativa (dvs långsamma) renderingsalgoritmer ska användas eller inte. |

### Exempel

Visar hur man anger mappen för lagring av länkade bilder efter att ha sparats i .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Ställ in ett alternativ för att exportera formulärfält som vanlig text istället för HTML-inmatningselement.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Visar hur du använder en specifik kodning när du sparar ett dokument i .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Som standard kommer ett utdata .epub-dokument att ha allt innehåll i en HTML-del.
// Ett delat kriterium tillåter oss att segmentera dokumentet i flera HTML-delar.
// Vi kommer att ställa in kriterierna för att dela upp dokumentet i rubriker.
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

    // Skapa ett "HtmlFixedSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
    // för att ändra hur vi konverterar dokumentet till HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Om vi sparar dokumentet normalt kommer det att finnas en HTML-utdata
    // dokument med allt källdokumentets innehåll.
    // Ställ in egenskapen "DocumentSplitCriteria" till "DocumentSplitCriteria.SectionBreak" till
    // spara vårt dokument i flera HTML-filer: en för varje avsnitt.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Tilldela en anpassad återuppringning till egenskapen "DocumentPartSavingCallback" för att ändra logiken för att spara dokumentdelen.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Om vi konverterar ett dokument som innehåller bilder till html kommer vi att få en html-fil som länkar till flera bilder.
    // Varje bild kommer att vara i form av en fil i det lokala filsystemet.
    // Det finns också en återuppringning som kan anpassa namnet och filsystemets plats för varje bild.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Ställer in anpassade filnamn för utdatadokument som sparoperationen delar upp ett dokument i.
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

        // Nedan finns två sätt att specificera var Aspose.Words kommer att spara varje del av dokumentet.
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
/// Ställer in anpassade filnamn för bildfiler som en HTML-konvertering skapar.
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

        // Nedan finns två sätt att specificera var Aspose.Words kommer att spara varje del av dokumentet.
        // 1 - Ange ett filnamn för utdatafilen:
        args.ImageFileName = imageFileName;

        // 2 - Skapa en anpassad ström för utdatafilen:
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


