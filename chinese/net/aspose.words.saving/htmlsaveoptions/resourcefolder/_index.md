---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions ResourceFolder 财产. 指定一个物理文件夹当 document 导出为 HTML 时所有资源如图像字体和外部 CSS都保存在其中默认为空字符串 在 C#.
type: docs
weight: 420
url: /zh/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

指定一个物理文件夹，当 document 导出为 HTML 时，所有资源（如图像、字体和外部 CSS）都保存在其中。默认为空字符串。

```csharp
public string ResourceFolder { get; set; }
```

## 评论

`ResourceFolder`是指定应写入所有资源的文件夹的最简单方法。 另一种方法是使用单独的属性[`FontsFolder`](../fontsfolder/),[`ImagesFolder`](../imagesfolder/), 和[`CssStyleSheetFileName`](../cssstylesheetfilename/)。

`ResourceFolder`优先级低于通过指定的文件夹[`FontsFolder`](../fontsfolder/), [`ImagesFolder`](../imagesfolder/)， 和[`CssStyleSheetFileName`](../cssstylesheetfilename/)。例如，如果 Both `ResourceFolder`和[`FontsFolder`](../fontsfolder/)指定后，字体将被保存 至[`FontsFolder`](../fontsfolder/)，而图像和 CSS 将保存到`ResourceFolder`。

如果指定的文件夹`ResourceFolder`不存在，将自动创建。

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
