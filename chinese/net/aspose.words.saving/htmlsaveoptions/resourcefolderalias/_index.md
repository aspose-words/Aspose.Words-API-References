---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions ResourceFolderAlias 财产. 指定用于构建写入 HTML 文档的所有资源的 URI 的文件夹名称 默认为空字符串 在 C#.
type: docs
weight: 430
url: /zh/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

指定用于构建写入 HTML 文档的所有资源的 URI 的文件夹名称。 默认为空字符串。

```csharp
public string ResourceFolderAlias { get; set; }
```

## 评论

`ResourceFolderAlias`是指定如何构建所有资源文件的 URI 的最简单方法。可以通过以下方式分别为图像和字体指定相同的信息[`ImagesFolderAlias`](../imagesfolderalias/) 和[`FontsFolderAlias`](../fontsfolderalias/)属性，分别。但是，CSS 没有单独的属性。

`ResourceFolderAlias`优先级低于[`FontsFolderAlias`](../fontsfolderalias/) 和[`ImagesFolderAlias`](../imagesfolderalias/)。例如，如果两者`ResourceFolderAlias` 和[`FontsFolderAlias`](../fontsfolderalias/)指定后，字体的 URI 将使用 构建[`FontsFolderAlias`](../fontsfolderalias/)，而图像和 CSS 的 URI 将使用 构造`ResourceFolderAlias`。

如果`ResourceFolderAlias`为空，则[`ResourceFolder`](../resourcefolder/)属性值将使用 来构造资源URI。

如果`ResourceFolderAlias`被设定为 '。' （点），资源 URI 将仅包含文件名，不包含 任何路径。

## 例子

展示如何为 Aspose.Words 在将文档保存为 HTML 时创建的外部保存资源设置文件夹和文件夹别名。

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

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
