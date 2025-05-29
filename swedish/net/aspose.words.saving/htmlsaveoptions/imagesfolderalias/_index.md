---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions ImagesFolderAlias för att enkelt hantera bild-URI:er i dina HTML-dokument. Förenkla ditt arbetsflöde med denna viktiga funktion!
type: docs
weight: 370
url: /sv/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Anger namnet på mappen som används för att konstruera bild-URI:er som skrivs in i ett HTML-dokument. Standardvärdet är en tom sträng.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) I HTML-format behöver Aspose.Words spara alla bilder som är inbäddade i dokumentet som fristående filer.[`ImagesFolder`](../imagesfolder/) låter dig ange var bilderna ska sparas och`ImagesFolderAlias` låter dig ange hur bildens URI:er ska konstrueras.

Om`ImagesFolderAlias` inte är en tom sträng, så kommer bild-URI:n written till HTML att varaImagesFolderAlias + &lt;bildfilnamn&gt;.

Om`ImagesFolderAlias`är en tom sträng, så kommer bild-URI:n written till HTML att varaImagesFolder + &lt;bildfilnamn&gt;.

Om`ImagesFolderAlias` är satt till '.' (punkt), så kommer bildfilen name att skrivas till HTML utan sökväg oavsett andra alternativ.

Ett annat sätt att ange namnet på mappen för att konstruera bild-URI:er är att använda[`ResourceFolderAlias`](../resourcefolderalias/).

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
    ImagesFolderAlias = "http://example.com/bilder",
    ResourceFolderAlias = "http://example.com/resurser",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
