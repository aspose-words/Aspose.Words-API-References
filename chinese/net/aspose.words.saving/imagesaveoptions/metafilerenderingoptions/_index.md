---
title: ImageSaveOptions.MetafileRenderingOptions
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words for .NET
description: 探索 ImageSaveOptions MetafileRenderingOptions 属性来控制渲染输出中的元文件处理，从而增强图像质量。
type: docs
weight: 90
url: /zh/net/aspose.words.saving/imagesaveoptions/metafilerenderingoptions/
---
## ImageSaveOptions.MetafileRenderingOptions property

允许指定如何在渲染输出中处理元文件。

```csharp
public MetafileRenderingOptions MetafileRenderingOptions { get; }
```

## 评论

什么时候Vector指定后，Aspose.Words 首先使用其自己的图元文件渲染引擎将 renders 图元文件渲染为矢量图形，然后将vector 图形渲染为图像。

什么时候Bitmap指定后，Aspose.Words 使用 GDI+ 元文件渲染引擎将 renders 元文件直接渲染到图像中。

GDI+ 图元文件渲染引擎运行速度更快，支持几乎所有图元文件功能，但在低分辨率下，与页面上其他矢量图形（尤其是文本）相比，可能会产生不一致的结果。Aspose.Words 图元文件渲染引擎即使在低分辨率下也能产生更一致的结果，但运行速度较慢，并且可能无法准确渲染复杂的图元文件。

默认值为[`MetafileRenderingMode`](../../metafilerenderingmode/)是Bitmap。

## 例子

展示如何将包含 Windows 图元文件图像的文档保存为其他图像格式时设置渲染模式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Windows MetaFile.wmf");

// 当我们将文档保存为图像时，我们可以将 SaveOptions 对象传递给
// 确定保存操作将如何处理文档中的 Windows 元文件。
// 如果我们将“RenderingMode”属性设置为“MetafileRenderingMode.Vector”，
// 或“MetafileRenderingMode.VectorWithFallback”，我们将所有元文件渲染为矢量图形。
// 如果我们将“RenderingMode”属性设置为“MetafileRenderingMode.Bitmap”，我们将把所有元文件渲染为位图。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
options.MetafileRenderingOptions.RenderingMode = metafileRenderingMode;
// 当值设置为 true 时，Aspose.Words 使用 GDI+ 进行光栅操作模拟。
options.MetafileRenderingOptions.UseGdiRasterOperationsEmulation = true;

doc.Save(ArtifactsDir + "ImageSaveOptions.WindowsMetaFile.png", options);
```

### 也可以看看

* class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
