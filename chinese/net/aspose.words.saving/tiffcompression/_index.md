---
title: TiffCompression Enum
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.TiffCompression 枚举，实现最佳的 TIFF 文件保存效果。轻松选择最佳压缩类型，获得高质量的页面图像。
type: docs
weight: 6430
url: /zh/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

指定将页面图像保存为 TIFF 文件时应用的压缩类型。

```csharp
public enum TiffCompression
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 指定不压缩。 |
| Rle | `1` | 指定 RLE 压缩方案。 |
| Lzw | `2` | 指定 LZW 压缩方案。 在 Java 中由 Deflate（Zip）压缩模拟。 |
| Ccitt3 | `3` | 指定 CCITT3 压缩方案。 |
| Ccitt4 | `4` | 指定 CCITT4 压缩方案。 |

## 例子

展示如何选择压缩方案应用于转换为 TIFF 图像的文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Logo.jpg");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
// 将“TiffCompression”属性设置为“TiffCompression.None”以在保存时不应用压缩，
// 这可能会导致输出文件非常大。
// 将“TiffCompression”属性设置为“TiffCompression.Rle”以应用 RLE 压缩
// 将“TiffCompression”属性设置为“TiffCompression.Lzw”以应用 LZW 压缩。
// 将“TiffCompression”属性设置为“TiffCompression.Ccitt3”以应用 CCITT3 压缩。
// 将“TiffCompression”属性设置为“TiffCompression.Ccitt4”以应用 CCITT4 压缩。
options.TiffCompression = tiffCompression;

doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
