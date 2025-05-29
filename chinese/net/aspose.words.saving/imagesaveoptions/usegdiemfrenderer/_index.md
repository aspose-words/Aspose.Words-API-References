---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words for .NET
description: 使用 ImageSaveOptions 优化 EMF 保存。控制 GDI 或 Aspose.Words 渲染器设置，以增强图像质量和性能。
type: docs
weight: 190
url: /zh/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

获取或设置一个值，确定保存到 EMF 时是否使用 GDI+ 或 Aspose.Words 图元文件渲染器。

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## 评论

如果设置为`真的`使用 GDI+ 元文件渲染器。即将内容写入 GDI+ graphics 对象并保存到元文件。

如果设置为`错误的`使用 Aspose.Words 图元文件渲染器。也就是说，使用 Aspose.Words 将内容直接写入图元文件格式。

仅当保存为 EMF 时才有效。

GDI+ 保存仅适用于 .NET。

默认值为`真的`。

## 例子

展示将文档转换为 .emf 时如何选择渲染器。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 当我们将文档保存为 EMF 图像时，我们可以传递一个 SaveOptions 对象来选择图像的渲染器。
// 如果我们将“UseGdiEmfRenderer”标志设置为“true”，Aspose.Words 将使用 GDI+ 渲染器。
// 如果我们将“UseGdiEmfRenderer”标志设置为“false”，Aspose.Words 将使用其自己的元文件渲染器。
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);
```

### 也可以看看

* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
