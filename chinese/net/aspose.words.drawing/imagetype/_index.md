---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.ImageType 枚举. 指定 Microsoft Word 文档中图像的类型格式 在 C#.
type: docs
weight: 1080
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
| Emf | `2` | Windows 增强型图元文件. |
| Wmf | `3` | Windows 图元文件。 |
| Pict | `4` | Macintosh PICT。现有图像将保留在文档中，但不支持将新 PICT 图像插入文档中。 |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | 便携式网络图形. |
| Bmp | `7` | Windows 位图. |
| Eps | `8` | 封装的 PostScript. |

## 例子

演示如何将图像添加到形状并检查其类型。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // URL 中的图像是 .gif。将其插入文档中会将其转换为 .png。
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### 也可以看看

* property [ImageType](../imagedata/imagetype/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
