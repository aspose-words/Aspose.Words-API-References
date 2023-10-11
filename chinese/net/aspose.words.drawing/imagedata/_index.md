---
title: Class ImageData
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.ImageData 班级. 定义形状的图像
type: docs
weight: 1060
url: /zh/net/aspose.words.drawing/imagedata/
---
## ImageData class

定义形状的图像。

要了解更多信息，请访问[处理图像](https://docs.aspose.com/words/net/working-with-images/)文档文章。

```csharp
public class ImageData
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | 确定图像是否以黑白显示。 |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | 获取图像边框的集合。边框仅对内嵌图像有效。 |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | 获取或设置图片的亮度。 该属性的值必须是 0.0（最暗）到 1.0（最亮）之间的数字。 |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | 定义将被视为透明的图像的颜色值。 |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | 获取或设置指定图片的对比度。此属性的 value 必须是从 0.0（最小对比度）到 1.0（最大对比度）之间的数字。 |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | 定义从底部移除图片的比例。 |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | 定义从左侧移除图片的比例。 |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | 定义从右侧删除图片的比例。 |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | 定义从顶部移除图片的比例。 |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | 确定图片是否以灰度模式显示。 |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | 返回`真的`如果形状具有图像字节或链接图像。 |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | 获取或设置存储在形状中的图像的原始字节。 |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | 获取有关图像大小和分辨率的信息。 |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | 获取图像的类型。 |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | 返回`真的`如果图像链接到形状（当[`SourceFullName`](./sourcefullname/)已指定）. |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | 返回`真的`如果图像已链接且未存储在文档中。 |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | 获取或设置链接图像的源文件的路径和名称。 |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | 定义图像的标题。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [FitImageToShape](../../aspose.words.drawing/imagedata/fitimagetoshape/)() |  |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(Stream) | 将图像保存到指定的流中。 |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(string) | 将图像保存到文件中。 |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(Image) | 设置形状显示的图像。 |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(Stream) | 设置形状显示的图像。 |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(string) | 设置形状显示的图像。 |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | 返回任何图像的图像字节，无论图像是存储还是链接。 |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | 获取存储在形状中的图像Image对象. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | 创建并返回包含图像字节的流。 |

### 评论

使用[`ImageData`](../shape/imagedata/)属性来访问和修改形状内的图像。 您不创建`ImageData`直接上课。

图像可以存储在形状内、链接到外部文件或两者（链接并存储在文档中）。

无论图像是存储在形状内部还是链接起来，您始终可以使用以下命令访问actual 图像：[`ToByteArray`](./tobytearray/),[`ToStream`](./tostream/),[`ToImage`](./toimage/)或者[`Save`](./save/) methods. 如果图像存储在形状内部，您还可以使用[`ImageBytes`](./imagebytes/)财产。

要将图像存储在形状内，请使用[`SetImage`](./setimage/)方法。要将图像链接到形状，请设置[`SourceFullName`](./sourcefullname/)财产。

### 例子

演示如何从文档中提取图像，并将它们作为单独的文件保存到本地文件系统。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 从文档中获取形状集合，
// 并将每个形状的图像数据以图像的形式保存到本地文件系统。
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

演示如何将链接图像插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// 下面是将图像应用到形状以便其显示的两种方法。
// 1 - 设置形状以包含图像。
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// 我们存储在 shape 中的每个图像都会增加文档的大小。
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - 设置形状以链接到本地文件系统中的图像文件。
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// 链接到图像将节省空间并导致文档更小。
// 但是，文档只能正确显示图像
// 图像文件位于形状的“SourceFullName”属性指向的位置。
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)


