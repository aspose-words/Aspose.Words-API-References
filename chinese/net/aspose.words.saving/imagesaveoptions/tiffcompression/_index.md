---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words for .NET
description: 使用 ImageSaveOptions TiffCompression 属性优化您的 TIFF 图像，允许您选择最佳压缩方法以获得质量结果。
type: docs
weight: 180
url: /zh/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

获取或设置在将生成的图像保存为 TIFF 格式时应用的压缩类型。

```csharp
public TiffCompression TiffCompression { get; set; }
```

## 评论

仅当保存为 TIFF 时才有效。

默认值为Lzw。

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

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
