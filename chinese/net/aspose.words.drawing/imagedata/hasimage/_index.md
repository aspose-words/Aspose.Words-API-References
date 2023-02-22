---
title: ImageData.HasImage
second_title: Aspose.Words for .NET API 参考
description: ImageData 财产. 如果形状具有图像字节或链接图像则返回 true
type: docs
weight: 110
url: /zh/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

如果形状具有图像字节或链接图像，则返回 true。

```csharp
public bool HasImage { get; }
```

### 例子

显示如何将文档中的所有图像保存到文件系统。

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// 设置了“HasImage”标志的形状存储并显示所有文档的图像。
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

//遍历每个形状并保存其图像。
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
* 命名空间 [Aspose.Words.Drawing](../../imagedata/)
* 部件 [Aspose.Words](../../../)


