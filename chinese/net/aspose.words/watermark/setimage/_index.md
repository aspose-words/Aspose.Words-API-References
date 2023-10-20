---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: 用于 .NET 的 Aspose.Words
description: Watermark SetImage 方法. 将图像水印添加到文档中 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

将图像水印添加到文档中。

```csharp
public void SetImage(Image image)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | Image | 显示为水印的图像。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentNullException | 当图像为空时抛出。 |

### 也可以看看

* class [Watermark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

将图像水印添加到文档中。

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | Image | 显示为水印的图像。 |
| options | ImageWatermarkOptions | 定义图像水印的附加选项。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentNullException | 当图像为空时抛出。 |

## 评论

如果[`ImageWatermarkOptions`](../../imagewatermarkoptions/)为空，水印将使用默认选项设置。

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

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

将图像水印添加到文档中。

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imagePath | String | 显示为水印的图像文件的路径。 |
| options | ImageWatermarkOptions | 定义图像水印的附加选项。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentNullException | 当路径为空时抛出。 |

## 评论

如果[`ImageWatermarkOptions`](../../imagewatermarkoptions/)为空，水印将使用默认选项设置。

### 也可以看看

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
