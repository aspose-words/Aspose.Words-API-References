---
title: HtmlSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words for .NET
description: 使用 HtmlSaveOptions 轻松调整图像分辨率。使用可自定义的设置优化您的 HTML、MHTML 或 EPUB 导出文件，获得惊艳的视觉效果。
type: docs
weight: 340
url: /zh/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

指定导出为 HTML、MHTML 或 EPUB 时图像的输出分辨率。 默认值为`96 dpi`.

```csharp
public int ImageResolution { get; set; }
```

## 评论

此属性在以下情况下影响光栅图像[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) 是`真的`以及导出为光栅图像的效果图元文件。某些图像属性（例如 cropping 或旋转）需要保存转换后的图像，在这种情况下，转换后的图像将以 given 分辨率创建。

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

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
