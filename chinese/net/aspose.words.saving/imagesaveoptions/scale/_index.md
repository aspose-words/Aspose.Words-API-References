---
title: ImageSaveOptions.Scale
second_title: Aspose.Words for .NET API 参考
description: ImageSaveOptions 财产. 获取或设置生成图像的缩放系数
type: docs
weight: 140
url: /zh/net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

获取或设置生成图像的缩放系数。

```csharp
public float Scale { get; set; }
```

### 评论

默认值为 1.0。该值必须大于 0.

### 例子

演示如何将 Office Math 对象呈现到本地文件系统中的图像文件中。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// 创建一个“ImageSaveOptions”对象传递给节点渲染器的“Save”方法进行修改
// 它如何将 OfficeMath 节点呈现为图像。
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// 将“Scale”属性设置为 5，以将对象渲染为其原始大小的五倍。
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

展示如何在 Aspose.Words 将文档转换为文档时编辑图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 当我们将文档保存为图片时，我们可以传递一个 SaveOptions 对象到
// 在保存操作渲染图像时编辑图像。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // 我们可以调整这些属性来改变图像的亮度和对比度。
    // 两者的比例都是 0-1，默认为 0.5。
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // 我们可以使用这些属性调整水平和垂直分辨率。
    // 这将影响图像的尺寸。
    // 这些属性的默认值为 96.0，分辨率为 96dpi。
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // 我们可以使用这个属性来缩放图像。默认值为 1.0，用于 100% 的缩放。
    // 我们可以使用这个属性来否定改变分辨率会导致的图像尺寸的任何变化。
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### 也可以看看

* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../imagesaveoptions/)
* 部件 [Aspose.Words](../../../)


