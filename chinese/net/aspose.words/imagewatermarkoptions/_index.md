---
title: ImageWatermarkOptions Class
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ImageWatermarkOptions。使用多种选项轻松自定义图像水印，增强文档呈现效果。
type: docs
weight: 3670
url: /zh/net/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class

包含添加图像水印时可以指定的选项。

要了解更多信息，请访问[使用水印](https://docs.aspose.com/words/net/working-with-watermark/)文档文章。

```csharp
public class ImageWatermarkOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ImageWatermarkOptions](imagewatermarkoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [IsWashout](../../aspose.words/imagewatermarkoptions/iswashout/) { get; set; } | 获取或设置一个布尔值，该值负责水印的冲淡效果。 默认值为`真的`. |
| [Scale](../../aspose.words/imagewatermarkoptions/scale/) { get; set; } | 获取或设置以图像分数表示的比例因子。默认值为 0 - 自动。 |

## 例子

展示如何从本地文件系统中的图像创建水印。

```csharp
Document doc = new Document();

            // 使用 ImageWatermarkOptions 对象修改图像水印的外观，
            // 然后在从图像文件创建水印时传递它。
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // 我们有不同的选项来插入图像：
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
