---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words for .NET
description: 使用 ImageData Save 方法轻松保存图像。轻松将图像直接存储到您选择的流中，简化您的工作流程。
type: docs
weight: 200
url: /zh/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

将图像保存到指定的流中。

```csharp
public void Save(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 保存图像的流。 |

## 评论

处置流对象是调用者的责任吗？

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

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
