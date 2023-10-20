---
title: FileFormatUtil.ImageTypeToExtension
linktitle: ImageTypeToExtension
articleTitle: ImageTypeToExtension
second_title: 用于 .NET 的 Aspose.Words
description: FileFormatUtil ImageTypeToExtension 方法. 将 Aspose.Words 图像类型枚举值转换为文件扩展名返回的扩展名是带有前导点的小写字符串 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil.ImageTypeToExtension method

将 Aspose.Words 图像类型枚举值转换为文件扩展名。返回的扩展名是带有前导点的小写字符串。

```csharp
public static string ImageTypeToExtension(ImageType imageType)
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | 无法转换时抛出。 |

## 例子

演示如何从文档中提取图像，并将它们作为单独的文件保存到本地文件系统。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 从文档中获取形状的集合，
// 并将每个形状的图像数据与图像一起作为文件保存到本地文件系统。
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // 形状的图像数据可能包含多种可能的图像格式的图像。 
        // 我们可以根据图像的格式自动确定每个图像的文件扩展名。
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### 也可以看看

* enum [ImageType](../../../aspose.words.drawing/imagetype/)
* class [FileFormatUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
