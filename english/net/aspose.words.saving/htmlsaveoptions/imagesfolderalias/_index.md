---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words for .NET
description: HtmlSaveOptions ImagesFolderAlias property. Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string in C#.
type: docs
weight: 380
url: /net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Remarks

When you save a [`Document`](../../../aspose.words/document/) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [`ImagesFolder`](../imagesfolder/) allows you to specify where the images will be saved and `ImagesFolderAlias` allows to specify how the image URIs will be constructed.

If `ImagesFolderAlias` is not an empty string, then the image URI written to HTML will be ImagesFolderAlias + &lt;image file name&gt;.

If `ImagesFolderAlias` is an empty string, then the image URI written to HTML will be ImagesFolder + &lt;image file name&gt;.

If `ImagesFolderAlias` is set to '.' (dot), then the image file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct image URIs is to use [`ResourceFolderAlias`](../resourcefolderalias/).

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

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
