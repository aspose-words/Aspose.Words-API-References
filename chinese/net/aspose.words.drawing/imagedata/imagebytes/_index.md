---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: 用于 .NET 的 Aspose.Words
description: ImageData ImageBytes 财产. 获取或设置存储在 shape 中的图像的原始字节数 在 C#.
type: docs
weight: 120
url: /zh/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

获取或设置存储在 shape 中的图像的原始字节数。

```csharp
public byte[] ImageBytes { get; set; }
```

## 评论

将值设置为`无效的`或者一个空数组将从形状中删除图像。

退货`无效的`如果图像未存储在文档中（例如，在这种情况下图像可能是链接的）。

## 例子

演示如何从形状的原始图像数据创建图像文件。

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() 返回存储在 ImageBytes 属性中的数组。
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// 将形状的图像数据保存到本地文件系统中的图像文件中。
using (Stream imgStream = imgShape.ImageData.ToStream())
{
    using (FileStream outStream = new FileStream(ArtifactsDir + "Drawing.GetDataFromImage.png",
        FileMode.Create, FileAccess.ReadWrite))
    {
        imgStream.CopyTo(outStream);
    }
}
```

### 也可以看看

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
