---
title: ImageSaveOptions.ImageColorMode
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words for .NET
description: 探索 ImageSaveOptions 的 ImageColorMode 属性，轻松自定义和优化生成图像的颜色模式。立即提升您的视觉效果！
type: docs
weight: 50
url: /zh/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

获取或设置生成图像的颜色模式。

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

## 评论

此属性仅在保存为光栅图像格式时有效。

默认值为None。

## 例子

展示如何在渲染文档时设置颜色模式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 当我们将文档保存为图像时，我们可以将 SaveOptions 对象传递给
// 为保存操作将生成的图像选择一种颜色模式。
// 如果我们将“ImageColorMode”属性设置为“ImageColorMode.BlackAndWhite”，
// 保存操作将在渲染文档时应用灰度颜色减少。
 // 如果我们将“ImageColorMode”属性设置为“ImageColorMode.Grayscale”，
// 保存操作将把文档渲染为单色图像。
// 如果我们将“ImageColorMode”属性设置为“None”，则保存操作将应用默认方法
// 并在输出图像中保留所有文档的颜色。
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### 也可以看看

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
