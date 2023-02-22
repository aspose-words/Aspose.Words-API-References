---
title: ImageData.ToStream
second_title: Aspose.Words for .NET API 参考
description: ImageData 方法. 创建并返回一个包含图像字节的流
type: docs
weight: 230
url: /zh/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

创建并返回一个包含图像字节的流。

```csharp
public Stream ToStream()
```

### 评论

如果图像字节存储在形状中，则创建并返回一个MemoryStream目的。

如果图像已链接并存储在文件中，则打开文件并返回FileStream目的。

如果图像被链接并存储在外部 URL 中，则下载文件并返回MemoryStream目的。

调用者是否有责任处置流对象。

### 例子

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
* 命名空间 [Aspose.Words.Drawing](../../imagedata/)
* 部件 [Aspose.Words](../../../)


