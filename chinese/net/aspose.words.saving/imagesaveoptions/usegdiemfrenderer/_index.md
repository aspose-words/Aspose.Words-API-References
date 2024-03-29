---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: 用于 .NET 的 Aspose.Words
description: ImageSaveOptions UseGdiEmfRenderer 财产. 获取或设置一个值确定在保存到 EMF 时是否使用 GDI 或 Aspose.Words 图元文件渲染器 在 C#.
type: docs
weight: 190
url: /zh/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

获取或设置一个值，确定在保存到 EMF 时是否使用 GDI+ 或 Aspose.Words 图元文件渲染器。

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## 评论

如果设置为`真的`使用 GDI+ 图元文件渲染器。即内容写入GDI+graphics 对象并保存到图元文件。

如果设置为`错误的`使用 Aspose.Words 图元文件渲染器。即内容直接 使用 Aspose.Words 写入图元文件格式。

仅在保存到 EMF 时有效。

GDI+ 保存仅适用于 .NET。

默认值为`真的`。

## 例子

演示将文档转换为 .emf 时如何选择渲染器。

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            // 当我们将文档保存为 EMF 图像时，我们可以传递一个 SaveOptions 对象来为图像选择渲染器。
            // 如果我们将“UseGdiEmfRenderer”标志设置为“true”，Aspose.Words 将使用 GDI+ 渲染器。
            // 如果我们将“UseGdiEmfRenderer”标志设置为“false”，Aspose.Words 将使用自己的图元文件渲染器。
            ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
            saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

            doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);

            // GDI+ 渲染器通常会创建较大的文件。
            if (useGdiEmfRenderer)
#if NET48 || JAVA
                Assert.That(300000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#elif NET5_0_OR_GREATER
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
#endif
            else
                Assert.That(30000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.Renderer.emf").Length));
```

### 也可以看看

* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
