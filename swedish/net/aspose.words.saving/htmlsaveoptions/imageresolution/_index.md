---
title: HtmlSaveOptions.ImageResolution
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger utdataupplösningen för bilder vid export till HTML MHTML eller EPUB. Standard är96 dpi .
type: docs
weight: 340
url: /sv/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Anger utdataupplösningen för bilder vid export till HTML, MHTML eller EPUB. Standard är`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

### Anmärkningar

Den här egenskapen påverkar rasterbilder när[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) är`Sann` och effektmetafiler exporterade som rasterbilder. Vissa bildegenskaper som cropping eller rotation kräver att transformerade bilder sparas och i detta fall skapas transformerade bilder i den givna upplösningen.

### Exempel

Visar hur man ställer in mappar och mappalias för externt sparade resurser som Aspose.Words skapar när ett dokument sparas till HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://example.com/fonts",
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://example.com/resurser",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Se även

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


