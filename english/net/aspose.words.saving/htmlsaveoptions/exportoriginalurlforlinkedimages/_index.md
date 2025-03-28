---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
linktitle: ExportOriginalUrlForLinkedImages
articleTitle: ExportOriginalUrlForLinkedImages
second_title: Aspose.Words for .NET
description: Discover HtmlSaveOptions' ExportOriginalUrlForLinkedImages feature, allowing you to use original URLs for linked images. Enhance your document's integrity!
type: docs
weight: 200
url: /net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Specifies whether original URL should be used as the URL of the linked images. Default value is `false`.

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

## Remarks

If value is set to `true`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) value is used as the URL of linked images and linked images are not loaded into document's folder or [`ImagesFolder`](../imagesfolder/).

If value is set to `false` linked images are loaded into document's folder or [`ImagesFolder`](../imagesfolder/) and URL of each linked image is constructed depending on document's folder, [`ImagesFolder`](../imagesfolder/) and [`ImagesFolderAlias`](../imagesfolderalias/) properties.

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
