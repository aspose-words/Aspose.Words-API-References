---
title: ImageData.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: 用于 .NET 的 Aspose.Words
description: ImageData ToByteArray 方法. 返回任何图像的图像字节无论图像是存储还是链接 在 C#.
type: docs
weight: 210
url: /zh/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

返回任何图像的图像字节，无论图像是存储还是链接。

```csharp
public byte[] ToByteArray()
```

## 评论

如果图像已链接，则每次调用时都会下载图像。

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
