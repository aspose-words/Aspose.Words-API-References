---
title: Enum ImageColorMode
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.ImageColorMode 枚举. 指定生成的文档页面图像的颜色模式
type: docs
weight: 5210
url: /zh/net/aspose.words.saving/imagecolormode/
---
## ImageColorMode enumeration

指定生成的文档页面图像的颜色模式。

```csharp
public enum ImageColorMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 文档页面将呈现为彩色图像。 |
| Grayscale | `1` | 文档页面将呈现为灰度图像。 |
| BlackAndWhite | `2` | 文档页面将呈现为黑白图像。 |

### 例子

演示如何在渲染文档时设置颜色模式。

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // 当我们将文档保存为图像时，我们可以将 SaveOptions 对象传递给
            // 为保存操作将生成的图像选择颜色模式。
            // 如果我们将“ImageColorMode”属性设置为“ImageColorMode.BlackAndWhite”，
            // 保存操作将在渲染文档时应用灰度颜色缩减。
            // 如果我们将“ImageColorMode”属性设置为“ImageColorMode.Grayscale”，
            // 保存操作会将文档渲染成单色图像。
            // 如果我们将“ImageColorMode”属性设置为“None”，则保存操作将应用默认方法
            // 并在输出图像中保留所有文档的颜色。
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.ImageColorMode = imageColorMode;

            doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(120000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#endif
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


