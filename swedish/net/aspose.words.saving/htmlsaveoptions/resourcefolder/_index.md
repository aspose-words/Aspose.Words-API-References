---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions ResourceFolder för optimal dokumentexport. Hantera enkelt bilder, teckensnitt och CSS i en särskild mapp.
type: docs
weight: 440
url: /sv/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

Anger en fysisk mapp där alla resurser som bilder, teckensnitt och extern CSS sparas när ett dokument exporteras till HTML. Standardvärdet är en tom sträng.

```csharp
public string ResourceFolder { get; set; }
```

## Anmärkningar

`ResourceFolder` är det enklaste sättet att ange en mapp där alla resurser ska skrivas. Ett annat sätt är att använda individuella egenskaper[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) , och[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` har lägre prioritet än mappar som anges via[`FontsFolder`](../fontsfolder/) , [`ImagesFolder`](../imagesfolder/) och[`CssStyleSheetFileName`](../cssstylesheetfilename/) Till exempel, om både `ResourceFolder` och[`FontsFolder`](../fontsfolder/)anges, kommer teckensnitt att sparas till[`FontsFolder`](../fontsfolder/) , medan bilder och CSS sparas till`ResourceFolder`.

Om mappen som anges av`ResourceFolder` inte finns, kommer den att skapas automatiskt.

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
