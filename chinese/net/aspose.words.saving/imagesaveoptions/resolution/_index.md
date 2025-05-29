---
title: ImageSaveOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words for .NET
description: 使用 ImageSaveOptions 优化您的图片！以 DPI 为单位控制水平和垂直分辨率，获得令人惊叹的画质和清晰度。立即提升您的视觉效果！
type: docs
weight: 130
url: /zh/net/aspose.words.saving/imagesaveoptions/resolution/
---
## ImageSaveOptions.Resolution property

设置生成图像的水平和垂直分辨率，以每英寸点数为单位。

```csharp
public float Resolution { set; }
```

## 评论

此属性仅在保存为光栅图像格式时有效。

## 例子

展示如何在将文档渲染为 PNG 时指定分辨率。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// 将“分辨率”属性设置为“72”以 72dpi 呈现文档。
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// 将“分辨率”属性设置为“300”以 300dpi 呈现文档。
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

### 也可以看看

* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
