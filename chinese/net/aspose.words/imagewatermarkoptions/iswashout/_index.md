---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: 用于 .NET 的 Aspose.Words
description: ImageWatermarkOptions IsWashout 财产. 获取或设置一个布尔值该值负责水印的冲刷效果 默认值为真的 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

获取或设置一个布尔值，该值负责水印的冲刷效果。 默认值为`真的`.

```csharp
public bool IsWashout { get; set; }
```

## 例子

演示如何从本地文件系统中的图像创建水印。

```csharp
Document doc = new Document();

            // 使用 ImageWatermarkOptions 对象修改图像水印的外观，
            // 然后在从图像文件创建水印时传递它。
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### 也可以看看

* class [ImageWatermarkOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
