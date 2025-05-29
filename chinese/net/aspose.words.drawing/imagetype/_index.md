---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.ImageType 枚举，轻松管理 Microsoft Word 文档中的图像格式。提升文档的视觉吸引力！
type: docs
weight: 1410
url: /zh/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

指定 Microsoft Word 文档中图像的类型（格式）。

```csharp
public enum ImageType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| NoImage | `0` | 没有图像数据。 |
| Unknown | `1` | 未知图像类型或无法直接存储在 Microsoft Word 文档中的图像类型。 |
| Emf | `2` | Windows 增强型图元文件。 |
| Wmf | `3` | Windows 图元文件. |
| Pict | `4` | Macintosh PICT。现有图像将保留在文档中，但不支持将新的 PICT 图像插入文档。 |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | 便携式网络图形。 |
| Bmp | `7` | Windows 位图. |
| Eps | `8` | 封装的 PostScript。 |
| WebP | `9` | WebP. |
| Gif | `10` | GIF |

## 例子

展示如何读取 WebP 图像。

```csharp
Document doc = new Document(MyDir + "Document with WebP image.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Assert.AreEqual(ImageType.WebP, shape.ImageData.ImageType);
```

展示如何向形状添加图像并检查其类型。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape imgShape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
```

### 也可以看看

* property [ImageType](../imagedata/imagetype/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
