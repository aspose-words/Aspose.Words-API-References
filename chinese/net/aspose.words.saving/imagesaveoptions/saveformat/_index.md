---
title: ImageSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: 探索 ImageSaveOptions 的 SaveFormat 属性，轻松将文档保存为 TIFF、PNG、JPEG 等格式。立即提升您的工作流程！
type: docs
weight: 140
url: /zh/net/aspose.words.saving/imagesaveoptions/saveformat/
---
## ImageSaveOptions.SaveFormat property

如果使用此保存选项对象，则指定渲染的文档页面或形状的保存格式。 可以是光栅 Tiff，Png，Bmp , Jpeg或向量Emf，Eps , WebP，Svg.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## 评论

其他选项的数量取决于所选的格式。

此外，还可以通过以下方式保存为 SVG[`ImageSaveOptions`](../)并通过[`SvgSaveOptions`](../../svgsaveoptions/)。

## 例子

展示如何在 Aspose.Words 将文档转换为图像时编辑图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 当我们将文档保存为图像时，我们可以将 SaveOptions 对象传递给
// 在保存操作渲染图像时编辑图像。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // 我们可以调整这些属性来改变图像的亮度和对比度。
    // 两者均采用 0-1 的尺度，默认为 0.5。
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // 我们可以使用这些属性来调整水平和垂直分辨率。
    // 这将影响图像的尺寸。
    // 这些属性的默认值为 96.0，分辨率为 96dpi。
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // 我们可以使用此属性缩放图像。默认值为 1.0，即缩放比例为 100%。
    // 我们可以使用此属性来消除因改变分辨率而导致的图像尺寸的任何变化。
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
