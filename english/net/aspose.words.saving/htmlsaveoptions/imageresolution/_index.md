---
title: HtmlSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words for .NET
description: HtmlSaveOptions ImageResolution property. Specifies the output resolution for images when exporting to HTML MHTML or EPUB. Default is 96 dpi in C#.
type: docs
weight: 350
url: /net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is `96 dpi`.

```csharp
public int ImageResolution { get; set; }
```

## Remarks

This property effects raster images when [`ScaleImageToShapeSize`](../scaleimagetoshapesize/) is `true` and effects metafiles exported as raster images. Some image properties such as cropping or rotation require saving transformed images and in this case transformed images are created in the given resolution.

## Examples

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

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
    ResourceFolderAlias = "http://example.com/resources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### See Also

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../htmlsaveoptions/)
* assembly [Aspose.Words](../../../)
