---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words for .NET
description: 使用 HtmlSaveOptions ResourceFolderAlias 属性优化您的 HTML 文档，定义文件夹名称以有效地构建资源 URI。
type: docs
weight: 450
url: /zh/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

指定用于构建写入 HTML 文档的所有资源的 URI 的文件夹的名称。 默认值为空字符串。

```csharp
public string ResourceFolderAlias { get; set; }
```

## 评论

`ResourceFolderAlias`是指定所有资源文件的 URI 构造方式的最简单方法。可以通过以下方式分别指定图像和字体的相同信息：[`ImagesFolderAlias`](../imagesfolderalias/) 和[`FontsFolderAlias`](../fontsfolderalias/)属性。但是，CSS 没有单独的属性。

`ResourceFolderAlias`优先级低于[`FontsFolderAlias`](../fontsfolderalias/) 和[`ImagesFolderAlias`](../imagesfolderalias/)。例如，如果`ResourceFolderAlias` 和[`FontsFolderAlias`](../fontsfolderalias/)指定后，字体的 URI 将使用 构建[`FontsFolderAlias`](../fontsfolderalias/)，而图像和 CSS 的 URI 将使用 构建`ResourceFolderAlias`。

如果`ResourceFolderAlias`为空，[`ResourceFolder`](../resourcefolder/)属性值将用于 来构建资源URI。

如果`ResourceFolderAlias`设置为“.”（点），资源 URI 将仅包含文件名，而不包含任何路径。

## 例子

展示如何设置 Aspose.Words 在将文档保存为 HTML 时创建的外部保存资源的文件夹和文件夹别名。

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
