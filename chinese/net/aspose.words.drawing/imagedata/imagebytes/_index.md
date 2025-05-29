---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words for .NET
description: 发现 ImageData ImageBytes 属性，轻松管理和操作形状内的原始图像字节，以增强视觉内容。
type: docs
weight: 120
url: /zh/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

获取或设置存储在形状中的图像的原始字节。

```csharp
public byte[] ImageBytes { get; set; }
```

## 评论

将值设置为`无效的`或者空数组将从形状中删除图像。

返回`无效的`如果图像未存储在文档中（例如，在这种情况下图像可能已链接）。

## 例子

展示如何从形状的原始图像数据创建图像文件。

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
