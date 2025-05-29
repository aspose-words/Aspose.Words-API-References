---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
linktitle: ExportOriginalUrlForLinkedImages
articleTitle: ExportOriginalUrlForLinkedImages
second_title: Aspose.Words för .NET
description: Upptäck HtmlSaveOptions funktion ExportOriginalUrlForLinkedImages, som låter dig använda original-URL:er för länkade bilder. Förbättra ditt dokuments integritet!
type: docs
weight: 200
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Anger om original-URL:en ska användas som URL för de länkade bilderna. Standardvärdet är`falsk` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

## Anmärkningar

Om värdet är satt till`sann`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) värdet används som URL för länkade bilder och länkade bilder laddas inte i dokumentets mapp eller[`ImagesFolder`](../imagesfolder/).

Om värdet är satt till`falsk`länkade bilder laddas in i dokumentets mapp eller[`ImagesFolder`](../imagesfolder/) och URL:en för varje länkad bild konstrueras beroende på dokumentets mapp,[`ImagesFolder`](../imagesfolder/) och[`ImagesFolderAlias`](../imagesfolderalias/) egenskaper.

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
