---
title: XamlFlowSaveOptions
second_title: Aspose.Words för .NET API Referens
description: Kan användas för att ange ytterligare alternativ när du sparar ett dokument i XamlFlow ellerXamlFlowPack format.
type: docs
weight: 5420
url: /sv/net/aspose.words.saving/xamlflowsaveoptions/
---
## XamlFlowSaveOptions class

Kan användas för att ange ytterligare alternativ när du sparar ett dokument i XamlFlow ellerXamlFlowPack format.

```csharp
public class XamlFlowSaveOptions : SaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [XamlFlowSaveOptions](xamlflowsaveoptions#constructor)() | Initierar en ny instans av denna klass som kan användas för att spara ett dokument iXamlFlow format. |
| [XamlFlowSaveOptions](xamlflowsaveoptions#constructor_1)(SaveFormat) | Initierar en ny instans av denna klass som kan användas för att spara ett dokument iXamlFlow ellerXamlFlowPack format. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar om man ska tillåta inbäddning av teckensnitt med PostScript outlines när inbäddning av TrueType-teckensnitt i ett dokument på det sparas. Standardvärdet är **falsk** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Hämtar eller ställer in anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Hämtar eller ställer in sökvägen till standardmall (inklusive filnamn). Standardvärdet för den här egenskapen är **tom sträng** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur 3D-effekter renderas. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-former renderas. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | När sant, gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är **Sann** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas av[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Endast som standardFlatOpc dokumentformat får mappas. |
| [ImageSavingCallback](../../aspose.words.saving/xamlflowsaveoptions/imagesavingcallback) { get; set; } | Gör det möjligt att styra hur bilder sparas när ett dokument sparas till XAML. |
| [ImagesFolder](../../aspose.words.saving/xamlflowsaveoptions/imagesfolder) { get; set; } | Anger den fysiska mappen där bilder sparas vid export av ett dokument till XAML-format. Standard är en tom sträng. |
| [ImagesFolderAlias](../../aspose.words.saving/xamlflowsaveoptions/imagesfolderalias) { get; set; } | Anger namnet på mappen som används för att konstruera bild-URI:er inskrivna i ett XAML-dokument. Standard är en tom sträng. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur bläckobjekt (InkML) renderas. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Hämtar eller ställer in värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är **falsk** . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | När`Sann` , snygga format utdata där tillämpligt. Standardvärdet är **falsk** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Anropas när ett dokument sparas och accepterar data om lagringsförlopp. |
| override [SaveFormat](../../aspose.words.saving/xamlflowsaveoptions/saveformat) { get; set; } | Anger formatet som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan endastXamlFlow . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Anger mappen för temporära filer som används när du sparar till en DOC- eller DOCX-fil. Som standard är denna egenskap`null` och inga temporära filer används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) egenskapen uppdateras innan du sparar. Standardvärdet är falskt; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Hämtar eller ställer in ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är **Sann** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) egenskapen uppdateras innan du sparar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) egenskapen uppdateras innan du sparar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Hämtar eller ställer in värde som avgör om innehållet i[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) uppdateras innan du sparar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Hämtar eller ställer in ett värde som avgör om kantutjämning ska användas eller inte för rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Hämtar eller ställer in ett värde som avgör huruvida högkvalitativa (dvs långsamma) renderingsalgoritmer ska användas eller inte. |

### Exempel

Visar hur man skriver ut filnamnen på länkade bilder som skapats när ett dokument konverteras till flödesformat .xaml.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Skapa ett "XamlFlowSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
    // för att ändra hur vi sparar dokumentet till XAML-sparformatet.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Använd egenskapen "ImagesFolder" för att tilldela en mapp i det lokala filsystemet som
    // Aspose.Words kommer att spara alla dokumentets länkade bilder.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Använd egenskapen "ImagesFolderAlias" för att använda den här mappen
    // när du konstruerar bild-URI:er istället för bildmappens namn.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // En mapp specificerad av "ImagesFolderAlias" kommer att behöva innehålla resurserna istället för "ImagesFolder".
    // Vi måste se till att mappen finns innan återuppringningens strömmar kan lägga sina resurser i den.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");

/// <summary>
/// Räknar och skriver ut filnamn på bilder medan deras överordnade dokument konverteras till flödesformen .xaml.
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // Om vi angav ett bildmappalias skulle vi också behöva
        // för att omdirigera varje ström för att placera dess bild i aliasmappen.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Se även

* class [SaveOptions](../saveoptions)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
