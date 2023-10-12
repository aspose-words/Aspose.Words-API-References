---
title: HtmlSaveOptions.FontsFolder
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger den fysiska mapp där teckensnitt sparas vid export av ett dokument till HTML. Standard är en tom sträng.
type: docs
weight: 310
url: /sv/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Anger den fysiska mapp där teckensnitt sparas vid export av ett dokument till HTML. Standard är en tom sträng.

```csharp
public string FontsFolder { get; set; }
```

### Anmärkningar

När du sparar en[`Document`](../../../aspose.words/document/) i HTML-format och[`ExportFontResources`](../exportfontresources/) är inställd på`Sann` , Aspose.Words måste spara teckensnitt som används i dokumentet som fristående filer. `FontsFolder` låter dig ange var typsnitten ska sparas och [`FontsFolderAlias`](../fontsfolderalias/) gör det möjligt att specificera hur teckensnittets URI:er kommer att konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words som standard -teckensnitten i samma mapp där dokumentfilen sparas. Använda sig av`FontsFolder` för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström så har Aspose.Words ingen mapp där du kan spara typsnitten, men behöver ändå spara typsnitten någonstans. I det här fallet måste du ange en tillgänglig mapp i`FontsFolder` egendom eller tillhandahålla anpassade strömmar via the[`FontSavingCallback`](../fontsavingcallback/) händelsehanterare.

Om mappen som anges av`FontsFolder` inte finns skapas den automatiskt.

[`ResourceFolder`](../resourcefolder/) är ett annat sätt att ange en mapp där teckensnitt ska sparas.

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

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


