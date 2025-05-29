---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions FontsFolderAlias för att anpassa teckensnitts-URI:er i dina HTML-dokument. Förbättra din webbdesign med lätthet!
type: docs
weight: 320
url: /sv/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Anger namnet på mappen som används för att konstruera teckensnitts-URI:er som skrivs in i ett HTML-dokument. Standardvärdet är en tom sträng.

```csharp
public string FontsFolderAlias { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) i HTML-format och[`ExportFontResources`](../exportfontresources/) är inställd på`sann` Aspose.Words behöver spara teckensnitt som används i dokumentet som fristående filer. [`FontsFolder`](../fontsfolder/) låter dig ange var teckensnitten ska sparas and `FontsFolderAlias` låter dig ange hur teckensnitts-URI:erna ska konstrueras.

Om`FontsFolderAlias` inte är en tom sträng, så kommer teckensnitts-URI:n som skrivits till HTML att varaTeckensnittMappAlias + &lt;teckensnittsfilnamn&gt;.

Om`FontsFolderAlias` är en tom sträng, så kommer teckensnitts-URI:n written till HTML att varaTeckensnittsmapp + &lt;teckensnittsfilnamn&gt;.

Om`FontsFolderAlias`är satt till '.' (punkt), så kommer teckensnittsfilen name att skrivas till HTML utan sökväg oavsett andra alternativ.

Ett annat sätt att ange namnet på mappen för att konstruera teckensnittet URIs är att använda[`ResourceFolderAlias`](../resourcefolderalias/).

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
