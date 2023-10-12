---
title: Enum ImagePixelFormat
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.ImagePixelFormat 枚举. 指定生成的文档页面图像的像素格式
type: docs
weight: 5220
url: /zh/net/aspose.words.saving/imagepixelformat/
---
## ImagePixelFormat enumeration

指定生成的文档页面图像的像素格式。

```csharp
public enum ImagePixelFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Format16BppRgb555 | `0` | 每像素 16 位，RGB。 |
| Format16BppRgb565 | `1` | 每像素 16 位，RGB。 |
| Format16BppArgb1555 | `2` | 每像素 16 位，ARGB。 |
| Format24BppRgb | `3` | 每像素 24 位，RGB。 |
| Format32BppRgb | `4` | 每像素 32 位，RGB。 |
| Format32BppArgb | `5` | 每像素 32 位，ARGB。 |
| Format32BppPArgb | `6` | 每像素 32 位，ARGB，预乘 alpha。 |
| Format48BppRgb | `7` | 每像素 48 位，RGB。 |
| Format64BppArgb | `8` | 每像素 64 位，ARGB。 |
| Format64BppPArgb | `9` | 每像素 64 位，ARGB，预乘 alpha。 |
| Format1bppIndexed | `10` | 每像素 1 位，索引。 |

### 例子

演示如何选择将文档渲染为图像的每像素比特率。

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // 当我们将文档保存为图像时，我们可以将 SaveOptions 对象传递给
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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


