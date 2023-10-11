---
title: ImageSaveOptions.ImageBrightness
second_title: Aspose.Words for .NET API 参考
description: ImageSaveOptions 财产. 获取或设置生成图像的亮度
type: docs
weight: 40
url: /zh/net/aspose.words.saving/imagesaveoptions/imagebrightness/
---
## ImageSaveOptions.ImageBrightness property

获取或设置生成图像的亮度。

```csharp
public float ImageBrightness { get; set; }
```

### 评论

此属性仅在保存为光栅图像格式时有效。

默认值为 0.5。该值必须在 0 到 1 之间的范围内。

### 例子

演示如何在 Aspose.Words 将文档转换为文档时编辑图像。

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
    // 两者的等级均为 0-1，默认为 0.5。
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // 我们可以使用这些属性调整水平和垂直分辨率。
    // 这会影响图像的尺寸。
    // 对于 96dpi 的分辨率，这些属性的默认值为 96.0。
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // 我们可以使用这个属性来缩放图像。默认值为 1.0，表示缩放为 100%。
    // 我们可以使用此属性来抵消更改分辨率所导致的图像尺寸的任何变化。
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### 也可以看看

* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../imagesaveoptions/)
* 部件 [Aspose.Words](../../../)


