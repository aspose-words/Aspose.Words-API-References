---
title: ImageData.ImageType
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words for .NET
description: 探索 ImageData 的 ImageType 属性，轻松识别图像类型，增强图像处理能力。立即提升您的开发效率！
type: docs
weight: 140
url: /zh/net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

获取图像的类型。

```csharp
public ImageType ImageType { get; }
```

## 例子

展示如何从文档中提取图像，并将其作为单独的文件保存到本地文件系统。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 从文档中获取形状集合，
// 并将每个带有图像的形状的图像数据作为文件保存到本地文件系统。
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

* enum [ImageType](../../imagetype/)
* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
