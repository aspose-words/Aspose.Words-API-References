---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions ImagesFolderAlias 财产. 指定用于构造写入 HTML 文档的图像 URI 的文件夹的名称 默认为空字符串 在 C#.
type: docs
weight: 370
url: /zh/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

指定用于构造写入 HTML 文档的图像 URI 的文件夹的名称。 默认为空字符串。

```csharp
public string ImagesFolderAlias { get; set; }
```

## 评论

当你保存一个[`Document`](../../../aspose.words/document/)在 HTML 格式中，Aspose.Words 需要将文档中嵌入的所有 图像保存为独立文件。[`ImagesFolder`](../imagesfolder/) 允许您指定图像的保存位置和`ImagesFolderAlias` 允许指定如何构建图像 URI。

如果`ImagesFolderAlias`不是空字符串，则图像 URI 写入 HTML 的 将是ImagesFolderAlias + &lt;图像文件名&gt;.

如果`ImagesFolderAlias`是一个空字符串，那么将 写入 HTML 的图像 URI 将是ImagesFolder + &lt;图像文件名&gt;.

如果`ImagesFolderAlias`被设定为 '。' （点），那么无论其他选项如何，图像文件名 都将写入 HTML 中而没有路径。

指定文件夹名称以构造图像 URIs 的另一种方法是使用[`ResourceFolderAlias`](../resourcefolderalias/).

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
