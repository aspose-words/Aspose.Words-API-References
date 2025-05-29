---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions FontsFolder för att enkelt hantera teckensnittslagring för HTML-export, vilket förbättrar dokumentpresentation och tillgänglighet.
type: docs
weight: 310
url: /sv/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Anger den fysiska mappen där teckensnitt sparas när ett dokument exporteras till HTML. Standardvärdet är en tom sträng.

```csharp
public string FontsFolder { get; set; }
```

## Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) i HTML-format och[`ExportFontResources`](../exportfontresources/) är inställd på`sann` Aspose.Words behöver spara teckensnitt som används i dokumentet som fristående filer. `FontsFolder` låter dig ange var teckensnitten ska sparas and [`FontsFolderAlias`](../fontsfolderalias/) låter dig ange hur teckensnitts-URI:erna ska konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words som standard teckensnitten i samma mapp där dokumentfilen är sparad.`FontsFolder` för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström har Aspose.Words ingen mapp där typsnitten ska sparas, , men behöver fortfarande spara dem någonstans. I det här fallet måste du ange en tillgänglig mapp i`FontsFolder` egendom eller tillhandahålla anpassade strömmar via the[`FontSavingCallback`](../fontsavingcallback/) händelsehanterare.

Om mappen som anges av`FontsFolder` inte finns, kommer den att skapas automatiskt.

[`ResourceFolder`](../resourcefolder/) är ett annat sätt att ange en mapp där teckensnitt ska sparas.

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
