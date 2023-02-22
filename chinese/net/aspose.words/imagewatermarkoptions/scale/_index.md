---
title: ImageWatermarkOptions.Scale
second_title: Aspose.Words for .NET API 参考
description: ImageWatermarkOptions 财产. 获取或设置以图像分数表示的比例因子默认值为 0  auto.
type: docs
weight: 30
url: /zh/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

获取或设置以图像分数表示的比例因子。默认值为 0 - auto.

```csharp
public double Scale { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | 当参数超出有效值范围时抛出。 |

### 评论

有效值范围从 0 到 65.5（含）。

自动缩放意味着水印将缩放到相对于 页边距的最大宽度和最大高度。

### 例子

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
* 命名空间 [Aspose.Words](../../imagewatermarkoptions/)
* 部件 [Aspose.Words](../../../)


