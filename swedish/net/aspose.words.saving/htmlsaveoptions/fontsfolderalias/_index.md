---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words för .NET
description: HtmlSaveOptions FontsFolderAlias fast egendom. Anger namnet på mappen som används för att konstruera teckensnittsURIer inskrivna i ett HTMLdokument. Standard är en tom sträng i C#.
type: docs
weight: 320
url: /sv/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Anger namnet på mappen som används för att konstruera teckensnitts-URI:er inskrivna i ett HTML-dokument. Standard är en tom sträng.

```csharp
public string FontsFolderAlias { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) i HTML-format och[`ExportFontResources`](../exportfontresources/) är inställd på`Sann` , Aspose.Words måste spara teckensnitt som används i dokumentet som fristående filer. [`FontsFolder`](../fontsfolder/) låter dig ange var typsnitten ska sparas och `FontsFolderAlias` gör det möjligt att specificera hur teckensnittets URI:er kommer att konstrueras.

Om`FontsFolderAlias` inte är en tom sträng, kommer typsnittet URI written till HTML att varaFontsFolderAlias + &lt;font filnamn&gt;.

Om`FontsFolderAlias` är en tom sträng, kommer teckensnittets URI som är skriven till HTML att varaFontsFolder + &lt;font filnamn&gt;.

Om`FontsFolderAlias`är satt till '.' (prick), så kommer teckensnittsfilnamnet att skrivas till HTML utan sökväg oavsett andra alternativ.

Ett alternativt sätt att ange namnet på mappen för att konstruera teckensnittet URIs är att använda[`ResourceFolderAlias`](../resourcefolderalias/).

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
