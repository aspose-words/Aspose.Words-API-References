---
title: Class HtmlFixedSaveOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.HtmlFixedSaveOptions klass. Kan användas för att ange ytterligare alternativ när du sparar ett dokument iHtmlFixed format.
type: docs
weight: 4820
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

Kan användas för att ange ytterligare alternativ när du sparar ett dokument iHtmlFixed format.

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar om man ska tillåta inbäddning av teckensnitt med PostScript outlines när inbäddning av TrueType-teckensnitt i ett dokument på det sparas. Standardvärdet är **falsk** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur färger återges. |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/) { get; set; } | Anger prefix som läggs till i alla klassnamn i filen style.css. Standardvärdet är`"åh"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Hämtar eller ställer in anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Hämtar eller ställer in sökvägen till standardmall (inklusive filnamn). Standardvärdet för den här egenskapen är **tom sträng** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur 3D-effekter renderas. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-former renderas. |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding/) { get; set; } | Anger kodningen som ska användas vid export till HTML. Standardvärdet är`ny UTF8Encoding(true)` (UTF-8 med BOM). |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/) { get; set; } | Anger om CSS (Cascading Style Sheet) ska bäddas in i HTML-dokument. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/) { get; set; } | Anger om teckensnitt ska bäddas in i HTML-dokument i Base64-format. Observera att denna flagga kan öka storleken på utdatafilen avsevärt. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/) { get; set; } | Anger om bilder ska bäddas in i HTML-dokument i Base64-format. Observera att denna flagga kan öka storleken på utdatafilen avsevärt. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/) { get; set; } | Anger om SVG-resurser ska bäddas in i HTML-dokument. Standardvärdet är`Sann` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields/) { get; set; } | Hämtar eller ställer in en indikation på om formulärfält exporteras som interactive objekt (som "input"-tagg) snarare än omvandlas till text eller grafik. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | När sant, gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är **Sann** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas av[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Endast som standardFlatOpc dokumentformat får mappas. |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat/) { get; set; } | Hämtar eller sätter[`ExportFontFormat`](../exportfontformat/) används för teckensnittsexport. Standardvärdet ärWoff . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur bläckobjekt (InkML) renderas. |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer kvaliteten på JPEG-bilderna i HTML-dokumentet. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Hämtar eller ställer in värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är **falsk** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Tillåter att ange alternativ för metafilrendering. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Hämtar eller sätter[`NumeralFormat`](../numeralformat/) används för återgivning av siffror. Europeiska siffror används som standard. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/) { get; set; } | Flagga anger om det krävs för att optimera utdata. Om denna flagga ställs in redundanta kapslade dukar och tomma dukar tas bort, sammanlänkas även grannglyfer med samma formatering. Obs! Noggrannheten i innehållsvisningen kan påverkas den här egenskapen är satt till true. Standard är true. |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/) { get; set; } | Anger den horisontella justeringen av sidor i ett HTML-dokument. Standardvärdet är`HtmlFixedHorizontalPageAlignment.Center` . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins/) { get; set; } | Anger marginalerna runt sidor i ett HTML-dokument. Marginalvärdet mäts i punkter och ska vara lika med eller större än 0. Standardvärdet är 10 poäng. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Gör det möjligt att styra hur separata sidor sparas när ett dokument exporteras till fast sidformat. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Hämtar eller ställer in sidorna att rendera. Standard är alla sidor i dokumentet. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | När`Sann` , snygga format utdata där tillämpligt. Standardvärdet är **falsk** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Anropas när ett dokument sparas och accepterar data om lagringsförlopp. |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Gör det möjligt att styra hur resurser (bilder, teckensnitt och css) sparas när ett dokument exporteras till fast sid-html-format. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/) { get; set; } | Anger den fysiska mappen där resurser (bilder, teckensnitt, css) sparas vid export av ett dokument till HTML-format. Standard är`null` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Anger namnet på mappen som används för att konstruera bild-URI:er inskrivna i ett HTML-dokument. Standard är`null` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/) { get; set; } | Flagga anger om "@font-face" CSS-regler ska placeras i en separat fil "fontFaces.css" när ett dokument sparas med extern stilmall (det vill säga när[`ExportEmbeddedCss`](./exportembeddedcss/) är`falsk` ). Standardvärdet är`falsk` , alla CSS-regler skrivs i en enda fil "styles.css". |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat/) { get; set; } | Anger formatet som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan endastHtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder/) { get; set; } | Anger om ram runt sidor ska visas. Standard är`Sann` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Anger mappen för temporära filer som används när du sparar till en DOC- eller DOCX-fil. Som standard är denna egenskap`null` och inga temporära filer används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan du sparar. Standardvärdet är falskt; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Hämtar eller ställer in ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är **Sann** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan du sparar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan du sparar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Hämtar eller ställer in värde som avgör om innehållet i[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) uppdateras innan du sparar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Hämtar eller ställer in ett värde som avgör om kantutjämning ska användas eller inte för rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Hämtar eller ställer in ett värde som avgör huruvida högkvalitativa (dvs långsamma) renderingsalgoritmer ska användas eller inte. |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/) { get; set; } | Flagga indikerar om teckensnitt från måldatorn måste användas för att visa dokumentet. Om denna flagga är satt till true,[`FontFormat`](./fontformat/) och[`ExportEmbeddedFonts`](./exportembeddedfonts/)egenskaper har ingen effekt, också[`ResourceSavingCallback`](./resourcesavingcallback/) aktiveras inte för teckensnitt. Standard är false. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Bestämmer om det angivna objektet har samma värde som det aktuella objektet. |

### Exempel

Visar hur man använder en återuppringning för att skriva ut URI:erna för externa resurser som skapats när ett dokument konverterades till HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // En mapp specificerad av ResourcesFolderAlias kommer att innehålla resurserna istället för ResourcesFolder.
    // Vi måste se till att mappen finns innan strömmarna kan lägga sina resurser i den.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Räknar och skriver ut URI:er för resurser som finns i när de konverteras till fast HTML.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Om vi ställer in ett mappalias i SaveOptions-objektet kommer vi att kunna skriva ut det härifrån.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Som standard använder 'ResourceFileUri' systemmappen för teckensnitt.
                // För att undvika problem på andra plattformar måste du uttryckligen ange sökvägen för typsnitten.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Om vi har angett en mapp i egenskapen "ResourcesFolderAlias",
        // vi kommer också att behöva omdirigera varje ström för att placera dess resurs i den mappen.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### Se även

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


