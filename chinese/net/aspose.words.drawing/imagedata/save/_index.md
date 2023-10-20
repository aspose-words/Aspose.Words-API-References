---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: 用于 .NET 的 Aspose.Words
description: ImageData Save 方法. 将图像保存到指定的流中 在 C#.
type: docs
weight: 190
url: /zh/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

将图像保存到指定的流中。

```csharp
public void Save(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 将图像保存到的流。 |

## 评论

调用者有责任处置流对象吗？

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

---

## Save(*string*) {#save_1}

将图像保存到文件中。

```csharp
public void Save(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 保存图像的文件名。 |

## 例子

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

### 也可以看看

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
