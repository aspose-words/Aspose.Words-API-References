---
title: ImageSaveOptions.ImageColorMode
second_title: Aspose.Words for .NET API 参考
description: ImageSaveOptions 财产. 获取或设置生成图像的颜色模式
type: docs
weight: 50
url: /zh/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

获取或设置生成图像的颜色模式。

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

### 评论

此属性仅在保存为光栅图像格式时有效。

默认值为None.

### 例子

显示如何在呈现文档时设置颜色模式。

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // 当我们将文档保存为图片时，我们可以传递一个 SaveOptions 对象到
            // 为保存操作将生成的图像选择一种颜色模式。
            // 如果我们将“ImageColorMode”属性设置为“ImageColorMode.BlackAndWhite”，
            // 保存操作将在渲染文档时应用灰度颜色减少。
             // 如果我们将“ImageColorMode”属性设置为“ImageColorMode.Grayscale”，
            // 保存操作会将文档渲染为单色图像。
            // 如果我们将“ImageColorMode”属性设置为“None”，保存操作将应用默认方法
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

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../imagesaveoptions/)
* 部件 [Aspose.Words](../../../)


