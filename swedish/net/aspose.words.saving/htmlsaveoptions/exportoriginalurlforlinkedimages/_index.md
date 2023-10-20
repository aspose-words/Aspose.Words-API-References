---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
linktitle: ExportOriginalUrlForLinkedImages
articleTitle: ExportOriginalUrlForLinkedImages
second_title: Aspose.Words för .NET
description: HtmlSaveOptions ExportOriginalUrlForLinkedImages fast egendom. Anger om den ursprungliga webbadressen ska användas som URL för de länkade bilderna. Standardvärdet ärfalsk  i C#.
type: docs
weight: 200
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Anger om den ursprungliga webbadressen ska användas som URL för de länkade bilderna. Standardvärdet är`falsk` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

## Anmärkningar

Om värdet är satt till`Sann`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) värdet används eftersom webbadressen till länkade bilder och länkade bilder inte läses in i dokumentets folder eller[`ImagesFolder`](../imagesfolder/).

Om värdet är satt till`falsk`länkade bilder läses in i dokumentets folder eller[`ImagesFolder`](../imagesfolder/) och URL för varje länkad bild är konstruerad beroende på dokumentets mapp,[`ImagesFolder`](../imagesfolder/) och[`ImagesFolderAlias`](../imagesfolderalias/) egenskaper.

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
