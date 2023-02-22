---
title: ImageSaveOptions.PixelFormat
second_title: Aspose.Words for .NET API 参考
description: ImageSaveOptions 财产. 获取或设置生成图像的像素格式
type: docs
weight: 110
url: /zh/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

获取或设置生成图像的像素格式。

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

### 评论

此属性仅在保存为光栅图像格式时有效。

默认值为Format32BppArgb.

由于 GDI+ 的工作，输出图像的像素格式可能与设置 value 不同。

### 例子

演示如何选择将文档呈现为图像的每像素比特率。

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // 当我们将文档保存为图片时，我们可以传递一个 SaveOptions 对象到
            // 为保存操作将生成的图像选择像素格式。
            // 不同的每像素比特率会影响生成图像的质量和文件大小。
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.PixelFormat = imagePixelFormat;

            // 我们可以克隆 ImageSaveOptions 实例。
            Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

            doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format32BppRgb:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imagePixelFormat)
            {
                case ImagePixelFormat.Format1bppIndexed:
                    Assert.That(10000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format24BppRgb:
                    Assert.That(70000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
                case ImagePixelFormat.Format16BppRgb555:
                case ImagePixelFormat.Format32BppRgb:
                case ImagePixelFormat.Format48BppRgb:
                    Assert.That(125000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.PixelFormat.png").Length));
                    break;
            }
#endif
```

### 也可以看看

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../imagesaveoptions/)
* 部件 [Aspose.Words](../../../)


