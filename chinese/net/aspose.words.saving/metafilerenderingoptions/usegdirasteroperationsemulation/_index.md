---
title: MetafileRenderingOptions.UseGdiRasterOperationsEmulation
linktitle: UseGdiRasterOperationsEmulation
articleTitle: UseGdiRasterOperationsEmulation
second_title: Aspose.Words for .NET
description: 探索 MetafileRenderingOptions UseGdiRasterOperationsEmulation 属性，以优化 GDI 的光栅操作。立即提升性能和灵活性！
type: docs
weight: 80
url: /zh/net/aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/
---
## MetafileRenderingOptions.UseGdiRasterOperationsEmulation property

获取或设置一个值，确定是否使用 GDI+ 进行光栅操作模拟。

```csharp
public bool UseGdiRasterOperationsEmulation { get; set; }
```

## 评论

Windows GDI+ 库可用于模拟光栅操作。它支持所有光栅操作 ，与 Aspose.Words 自身的模拟相比，但在某些情况下性能可能会较慢。

当此值设置为`真的`，Aspose.Words 使用 GDI+ 进行光栅操作模拟。

当此值设置为`错误的`，Aspose.Words 使用其自己的光栅操作模拟实现。

仅当图元文件呈现为矢量图形时才使用此选项。

默认值为`错误的`。

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

* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
