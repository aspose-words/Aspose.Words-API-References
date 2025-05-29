---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.ImageData 类——定义和管理形状中图像的解决方案。轻松增强您的文档设计！
type: docs
weight: 1390
url: /zh/net/aspose.words.drawing/imagedata/
---
## ImageData class

为形状定义图像。

要了解更多信息，请访问[处理图像](https://docs.aspose.com/words/net/working-with-images/)文档文章。

```csharp
public class ImageData
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | 确定图像是否以黑白显示。 |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | 获取图片边框集合。边框仅对内联图片有效。 |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | 获取或设置图片的亮度。 此属性的值必须是从 0.0（最暗）到 1.0（最亮）的数字。 |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | 定义将被视为透明的图像的颜色值。 |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | 获取或设置指定图片的对比度。此属性的 value 必须为 0.0（最低对比度）到 1.0（最高对比度）之间的数字。 |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | 定义从底部移除的图片比例。 |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | 定义从左侧移除的图片比例。 |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | 定义从右侧移除的图片比例。 |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | 定义从顶部移除的图片比例。 |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | 确定图片是否以灰度模式显示。 |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | 返回`真的`如果形状有图像字节或链接图像。 |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | 获取或设置存储在形状中的图像的原始字节。 |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | 获取有关图像大小和分辨率的信息。 |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | 获取图像的类型。 |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | 返回`真的`如果图像链接到形状（当[`SourceFullName`](./sourcefullname/)已指定）。 |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | 返回`真的`如果图像是链接的但未存储在文档中。 |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | 获取或设置链接图像的源文件的路径和名称。 |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | 定义图像的标题。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [FitImageToShape](../../aspose.words.drawing/imagedata/fitimagetoshape/)() | 将图像数据适合 Shape 框架，以便图像数据的纵横比与 Shape 框架的纵横比相匹配。 |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | 将图像保存到指定的流中。 |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | 将图像保存到文件中。 |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | 设置形状显示的图像。 |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | 设置形状显示的图像。 |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | 设置形状显示的图像。 |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | 返回任何图像的图像字节，无论该图像是否存储或链接。 |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | 获取形状中存储的图像Image对象. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | 创建并返回包含图像字节的流。 |

## 评论

使用[`ImageData`](../shape/imagedata/)属性来访问和修改形状内的图像。 您不创建`ImageData`直接上课。

图像可以存储在形状内部、链接到外部文件或两者兼而有之（链接并存储在文档中）。

无论图像是存储在形状内还是链接，您始终可以使用[`ToByteArray`](./tobytearray/)，[`ToStream`](./tostream/)，[`ToImage`](./toimage/)或者[`Save`](./save/)方法。 如果图像存储在形状内，您也可以使用[`ImageBytes`](./imagebytes/)财产。

要将图像存储在形状内，请使用[`SetImage`](./setimage/)方法。要将图像链接到形状，请设置[`SourceFullName`](./sourcefullname/)财产。

## 例子

展示如何从文档中提取图像，并将其作为单独的文件保存到本地文件系统。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 从文档中获取形状集合，
// 并将每个带有图像的形状的图像数据作为文件保存到本地文件系统。
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // 形状的图像数据可能包含多种可能的图像格式的图像。
        // 我们可以根据每个图像的格式自动确定其文件扩展名。
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

展示如何将链接图像插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// 以下是将图像应用到形状以便显示它的两种方法。
// 1 - 设置形状以包含图像。
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// 我们存储在形状中的每个图像都会增加文档的大小。
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - 设置形状以链接到本地文件系统中的图像文件。
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// 链接到图像将节省空间并产生更小的文档。
// 但是，文档只能在
// 图像文件位于形状的“SourceFullName”属性指向的位置。
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
