---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words for .NET
description: 解锁 ImageData 中 ToImage 方法的强大功能，轻松检索形状中存储的图像作为 Image 对象。轻松增强您的项目！
type: docs
weight: 230
url: /zh/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

获取形状中存储的图像Image对象.

```csharp
public Image ToImage()
```

## 评论

一个新的Image每次调用此方法时都会创建对象。

处理图像对象是调用者的责任。

## 例子

展示如何将文档中的所有图像保存到文件系统。

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// 设置了“HasImage”标志的形状存储并显示所有文档的图像。
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// 遍历每个形状并保存其图像。
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### 也可以看看

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
