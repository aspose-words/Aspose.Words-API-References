---
title: HtmlSaveOptions.ResourceFolderAlias
second_title: Aspose.Words for .NET API Reference
description: HtmlSaveOptions property. Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string in C#.
type: docs
weight: 430
url: /net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Remarks

`ResourceFolderAlias` is the simplest way to specify how URIs for all resource files should be constructed. Same information can be specified for images and fonts separately via [`ImagesFolderAlias`](../imagesfolderalias/) and [`FontsFolderAlias`](../fontsfolderalias/) properties, respectively. However, there is no individual property for CSS.

`ResourceFolderAlias` has lower priority than [`FontsFolderAlias`](../fontsfolderalias/) and [`ImagesFolderAlias`](../imagesfolderalias/). For example, if both `ResourceFolderAlias` and [`FontsFolderAlias`](../fontsfolderalias/) are specified, fonts' URIs will be constructed using [`FontsFolderAlias`](../fontsfolderalias/), while URIs of images and CSS will be constructed using `ResourceFolderAlias`.

If `ResourceFolderAlias` is empty, the [`ResourceFolder`](../resourcefolder/) property value will be used to construct resource URIs.

If `ResourceFolderAlias` is set to '.' (dot), resource URIs will contain file names only, without any path.

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
* namespace [Aspose.Words.Saving](../../htmlsaveoptions/)
* assembly [Aspose.Words](../../../)
