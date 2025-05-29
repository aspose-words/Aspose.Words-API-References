---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: Aspose.Words for .NET
description: 探索 HtmlSaveOptions ResourceFolder 属性，实现最佳文档导出效果。轻松管理指定文件夹中的图像、字体和 CSS。
type: docs
weight: 440
url: /zh/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

指定将文档导出为 HTML 时保存所有资源（例如图片、字体和外部 CSS）的物理文件夹。默认值为空字符串。

```csharp
public string ResourceFolder { get; set; }
```

## 评论

`ResourceFolder`是指定应写入所有资源的文件夹的最简单方法。 另一种方法是使用单独的属性[`FontsFolder`](../fontsfolder/)，[`ImagesFolder`](../imagesfolder/), 和[`CssStyleSheetFileName`](../cssstylesheetfilename/)。

`ResourceFolder`优先级低于通过[`FontsFolder`](../fontsfolder/), [`ImagesFolder`](../imagesfolder/)， 和[`CssStyleSheetFileName`](../cssstylesheetfilename/)。例如，如果both `ResourceFolder`和[`FontsFolder`](../fontsfolder/)指定后，字体将保存到[`FontsFolder`](../fontsfolder/)，而图像和 CSS 将保存到`ResourceFolder`。

如果指定的文件夹`ResourceFolder`不存在，将自动创建。

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
