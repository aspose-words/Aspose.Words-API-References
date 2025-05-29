---
title: ImageData.Brightness
linktitle: Brightness
articleTitle: Brightness
second_title: Aspose.Words for .NET
description: 使用 ImageData 的 Brightness 属性调整图像的亮度。为了获得最佳视觉效果，请将值设置为 0.0（最暗）到 1.0（最亮）。
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/imagedata/brightness/
---
## ImageData.Brightness property

获取或设置图片的亮度。 此属性的值必须是从 0.0（最暗）到 1.0（最亮）的数字。

```csharp
public double Brightness { get; set; }
```

## 评论

默认值为 0.5。

## 例子

展示如何编辑形状的图像数据。

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// 从源文档导入形状并将其附加到第一段。
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// 导入的形状包含一张图片。我们可以通过 ImageData 对象访问图片的属性和原始数据。
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// 如果图像没有边框，其 ImageData 对象将把边框颜色定义为空。
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// 此图像未链接到本地文件系统中的其他形状或图像文件。
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// “亮度”和“对比度”属性定义图像的亮度和对比度
// 范围为 0-1，默认值为 0.5。
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// 上述亮度和对比度值创建了具有大量白色的图像。
// 我们可以选择一种具有 ChromaKey 属性的颜色来替换透明度，例如白色。
imageData.ChromaKey = Color.White;

// 再次导入源形状并将图像设置为单色。
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// 再次导入源形状以创建第三张图像并将其设置为 BiLevel。
// BiLevel 将每个像素设置为黑色或白色，以更接近原始颜色为准。
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// 裁剪以 0-1 的比例确定。裁剪一侧 0.3
// 将在裁剪侧裁剪掉图像的 30%。
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### 也可以看看

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
