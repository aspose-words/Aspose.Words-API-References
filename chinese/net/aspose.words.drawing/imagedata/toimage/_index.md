---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: 用于 .NET 的 Aspose.Words
description: ImageData ToImage 方法. 获取存储在形状中的图像Image对象 在 C#.
type: docs
weight: 220
url: /zh/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

获取存储在形状中的图像Image对象.

```csharp
public Image ToImage()
```

## 评论

一个新的Image每次调用此方法时都会创建对象。

调用者有责任处理图像对象。

## 例子

演示如何将文档中的所有图像保存到文件系统。

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// 设置了“HasImage”标志的形状存储并显示文档的所有图像。
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// 遍历每个形状并保存其图像。
ImageFormatConverter formatConverter = new ImageFormatConverter();

using (IEnumerator<Shape> enumerator = shapesWithImages.GetEnumerator())
{
    int shapeIndex = 0;

    while (enumerator.MoveNext())
    {
        ImageData imageData = enumerator.Current.ImageData;
        ImageFormat format = imageData.ToImage().RawFormat;
        string fileExtension = formatConverter.ConvertToString(format);

        using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{++shapeIndex}.{fileExtension}"))
            imageData.Save(fileStream);
    }
}
```

### 也可以看看

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
