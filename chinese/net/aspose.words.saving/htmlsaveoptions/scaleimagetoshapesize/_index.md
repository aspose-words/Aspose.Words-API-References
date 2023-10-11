---
title: HtmlSaveOptions.ScaleImageToShapeSize
second_title: Aspose.Words for .NET API 参考
description: HtmlSaveOptions 财产. 指定在导出为 HTMLMHTML 或 EPUB 时Aspose.Words 是否将图像缩放至边界形状大小 默认值为真的.
type: docs
weight: 450
url: /zh/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

指定在导出为 HTML、MHTML 或 EPUB 时，Aspose.Words 是否将图像缩放至边界形状大小。 默认值为`真的`.

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

### 评论

Microsoft Word 文档中的图像是一种形状。形状有一个大小，image 有它自己的大小。尺寸没有直接联系。例如，图像可以是 1024x786 像素 ，但显示该图像的形状可以是 400x300 点。

为了在浏览器中显示图像，必须将其缩放到形状大小。 `ScaleImageToShapeSize`属性控制 image 的缩放发生位置：在导出为 HTML 期间在 Aspose.Words 中或在显示文档时在浏览器中。

什么时候`ScaleImageToShapeSize`是`真的` ，图像在导出为 HTML 期间由 Aspose.Words 使用高质量缩放进行缩放。什么时候`ScaleImageToShapeSize` 是`错误的`，图像以其原始尺寸输出，浏览器必须对其进行缩放。

一般来说，浏览器的缩放速度很快，但质量很差。因此，您通常会在浏览器中获得更好的 显示质量和更小的文件大小`ScaleImageToShapeSize`是`真的` 但打印质量更好并且转换速度更快`ScaleImageToShapeSize`是`错误的`。

除了包含单个光栅图像的形状外，此选项还会影响由光栅图像组成的 组形状。如果`ScaleImageToShapeSize`是`错误的`并且组形状包含光栅图像 ，其固有分辨率高于中指定的值[`ImageResolution`](../imageresolution/)Aspose.Words will 增加该组的渲染分辨率。这样可以在保存为 HTML 时更好地保持分组高分辨率 图像的质量。

### 例子

演示如何在保存为 .html 时禁用图像缩放至其父形状尺寸。

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // 插入一个包含图像的形状，然后使该形状比图像小得多。
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            Shape imageShape = builder.InsertImage(image);
            imageShape.Width = 50;
            imageShape.Height = 50;

            // 将包含带有图像的形状的文档保存到 HTML 将在本地文件系统中创建一个图像文件
            // 对于每个这样的形状。输出 HTML 文档将使用 <image>标签来链接并显示这些图像。
            // 当我们将文档保存为HTML时，我们可以传递一个SaveOptions对象来确定
            // 是否将形状内的所有图像缩放到其形状的大小。
            // 将“ScaleImageToShapeSize”标志设置为“true”将缩小每个图像
            // 到包含它的形状的大小，这样保存的图像就不会大于文档要求的大小。
            // 将“ScaleImageToShapeSize”标志设置为“false”将保留这些图像的原始尺寸，
            // 这将占用更多空间以换取保持图像质量。
            HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

            doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);

            FileInfo fileInfo = new FileInfo(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.001.png");

#if NET48 || JAVA
        if (scaleImageToShapeSize)
            Assert.That(3000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(20000, Is.LessThan(fileInfo.Length));
#elif NET5_0_OR_GREATER
        if (scaleImageToShapeSize)
            Assert.That(10000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(30000, Is.LessThan(fileInfo.Length));
#endif
```

### 也可以看看

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


