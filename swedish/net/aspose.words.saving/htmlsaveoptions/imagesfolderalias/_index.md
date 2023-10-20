---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words för .NET
description: HtmlSaveOptions ImagesFolderAlias fast egendom. Anger namnet på mappen som används för att konstruera bildURIer inskrivna i ett HTMLdokument. Standard är en tom sträng i C#.
type: docs
weight: 370
url: /sv/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Anger namnet på mappen som används för att konstruera bild-URI:er inskrivna i ett HTML-dokument. Standard är en tom sträng.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) i HTML-format måste Aspose.Words spara alla -bilder som är inbäddade i dokumentet som fristående filer.[`ImagesFolder`](../imagesfolder/) låter dig ange var bilderna ska sparas och`ImagesFolderAlias` tillåter att specificera hur bildens URI:er kommer att konstrueras.

Om`ImagesFolderAlias` inte är en tom sträng, så blir bilden URI written till HTMLImagesFolderAlias + &lt;bildfilnamn&gt;.

Om`ImagesFolderAlias` är en tom sträng, kommer bildens URI som är skriven till HTML att varaImagesFolder + &lt;bildfilnamn&gt;.

Om`ImagesFolderAlias`är satt till '.' (prick), då kommer bildfilens namn att skrivas till HTML utan sökväg oavsett andra alternativ.

Ett alternativt sätt att ange namnet på mappen för att konstruera bilden URIs är att använda[`ResourceFolderAlias`](../resourcefolderalias/).

## Exempel

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

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
