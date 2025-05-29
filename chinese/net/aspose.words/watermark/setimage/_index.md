---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words for .NET
description: 使用 Watermark SetImage 方法增强您的文档效果。轻松添加精美的图像水印，打造专业水印。
type: docs
weight: 30
url: /zh/net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

在文档中添加图像水印。

```csharp
public void SetImage(Image image)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | Image | 显示为水印的图像。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentNullException | 当图像`无效的`. |

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

* class [Watermark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

在文档中添加图像水印。

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
| ArgumentNullException | 当图像`无效的`. |

## 评论

如果[`ImageWatermarkOptions`](../../imagewatermarkoptions/)是`无效的`，水印将使用默认选项设置。

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

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_3}

在文档中添加图像水印。

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
| ArgumentNullException | 当路径`无效的`. |

## 评论

如果[`ImageWatermarkOptions`](../../imagewatermarkoptions/)是`无效的`，水印将使用默认选项设置。

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

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## SetImage(*Stream, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

在文档中添加图像水印。

```csharp
public void SetImage(Stream imageStream, ImageWatermarkOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageStream | Stream | 包含显示为水印的图像数据的流。 |
| options | ImageWatermarkOptions | 定义图像水印的附加选项。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentNullException | 当路径`无效的`. |

## 评论

如果[`ImageWatermarkOptions`](../../imagewatermarkoptions/)是`无效的`，水印将使用默认选项设置。

## 例子

展示如何从图像流创建水印。

```csharp
Document doc = new Document();

// 使用 ImageWatermarkOptions 对象修改图像水印的外观，
// 然后在从图像文件创建水印时传递它。
ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
imageWatermarkOptions.Scale = 5;

using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
    doc.Watermark.SetImage(imageStream, imageWatermarkOptions);

doc.Save(ArtifactsDir + "Document.ImageWatermarkStream.docx");
```

### 也可以看看

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
