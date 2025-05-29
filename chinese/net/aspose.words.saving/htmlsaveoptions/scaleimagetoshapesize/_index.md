---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words for .NET
description: 了解 HtmlSaveOptions 的 ScaleImageToShapeSize 属性如何优化 Aspose.Words 中 HTML、MHTML 或 EPUB 导出的图像缩放。增强您的文档！
type: docs
weight: 470
url: /zh/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

指定在导出为 HTML、MHTML 或 EPUB 时，Aspose.Words 是否将图像缩放到边界形状大小。 默认值为`真的`.

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## 评论

Microsoft Word 文档中的图像是一种形状。形状具有大小，并且 image 也具有其自身的大小。大小之间没有直接关联。例如，图像可以是 1024x786 像素，但显示该图像的形状可以是 400x300 像素。

为了在浏览器中显示图像，必须将其缩放到形状大小。 `ScaleImageToShapeSize`属性控制 image 的缩放位置：在导出为 HTML 期间在 Aspose.Words 中或在显示文档时在浏览器中。

什么时候`ScaleImageToShapeSize`是`真的` ，在导出为 HTML 时，图像将由 Aspose.Words 使用高质量缩放进行缩放。当`ScaleImageToShapeSize` 是`错误的`，图像以原始大小输出，浏览器必须对其进行缩放。

一般来说，浏览器的缩放速度很快，但质量较差。因此，通常情况下，在浏览器中，显示质量会更好，文件大小也会更小。`ScaleImageToShapeSize`是`真的` , 但打印质量更好，转换速度更快`ScaleImageToShapeSize`是`错误的`。

除了包含单个光栅图像的形状外，此选项还影响由光栅图像组成的组形状。如果`ScaleImageToShapeSize`是`错误的`并且组形状包含光栅图像 ，其固有分辨率高于指定的值[`ImageResolution`](../imageresolution/)Aspose.Words 将提高该组的渲染分辨率。这样，在保存为 HTML 时，分组的高分辨率图像可以更好地保留其质量。

## 例子

展示如何在保存为 .html 时禁用图像到其父形状尺寸的缩放。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个包含图像的形状，然后使该形状比图像小得多。
Shape imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");
imageShape.Width = 50;
imageShape.Height = 50;

// 将包含带图像的形状的文档保存为 HTML 将在本地文件系统中创建一个图像文件
// 对于每个这样的形状。输出 HTML 文档将使用 <image> 标签链接并显示这些图像。
// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象来确定
// 是否将形状内的所有图像缩放到其形状的大小。
// 将“ScaleImageToShapeSize”标志设置为“true”将缩小每个图像
// 为包含它的形状的大小，这样保存的图像就不会大于文档所要求的大小。
// 将“ScaleImageToShapeSize”标志设置为“false”将保留这些图像的原始大小，
// 这将占用更多空间以换取保持图像质量。
HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
```

### 也可以看看

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
