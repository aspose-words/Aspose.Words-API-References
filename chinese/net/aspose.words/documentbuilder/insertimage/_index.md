---
title: DocumentBuilder.InsertImage
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 插入来自 .NET 的图像Image 对象放入文档中图像以 100 比例内嵌插入
type: docs
weight: 380
url: /zh/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(Image) {#insertimage_3}

插入来自 .NET 的图像Image 对象放入文档中。图像以 100% 比例内嵌插入。

```csharp
public Shape InsertImage(Image image)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | Image | 要插入到文档中的图像。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将对象中的图像插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// 下面是从 Image 对象实例插入图像的三种方法。
// 1 - 内联形状，其默认大小基于图像的原始尺寸：
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - 具有自定义尺寸的内联形状：
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - 具有自定义尺寸的浮动形状：
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(string) {#insertimage_9}

将文件或 URL 中的图像插入到文档中。图像以 100% 比例内嵌插入。

```csharp
public Shape InsertImage(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 带有图像的文件。可以是任何有效的本地或远程 URI。 |

### 返回值

刚刚插入的图像节点。

### 评论

如果您指定远程 URI，此重载将在插入到 document 之前自动下载图像。

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将 gif 图像插入到文档中。

```csharp
DocumentBuilder builder = new DocumentBuilder();

// 我们可以使用路径或字节数组插入 gif 图像。
// 仅当 DocumentBuilder 针对 Word 版本 2010 或更高版本进行优化时才有效。
// 注意，访问图像字节会导致 Gif 转换为 Png。
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

演示如何将带有图像的形状插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 下面是文档生成器的“InsertShape”方法的两个位置
// 可以获取形状将显示的图像。
// 1 - 传递图像文件的本地文件系统文件名：
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 - 传递指向图像的 URL。
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

演示如何将浮动图像插入到页面中央。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个浮动图像，该图像将出现在重叠文本后面并将其与页面中心对齐。
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

演示如何确定将插入哪个图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words 将 SVG 图像以带有 svgBlip 扩展名的 PNG 格式插入到文档中
// 包含原始矢量 SVG 图像表示。
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words 将 SVG 图像作为 PNG 插入到文档中，就像 Microsoft Word 对旧格式所做的那样。
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words 将 SVG 图像作为 EMF 图元文件插入到文档中，以保持图像的矢量表示形式。
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

演示如何将本地文件系统中的图像插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是从本地系统文件名插入图像的三种方法。
// 1 - 内联形状，其默认大小基于图像的原始尺寸：
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - 具有自定义尺寸的内联形状：
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - 具有自定义尺寸的浮动形状：
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(Stream) {#insertimage_6}

将图像从流插入到文档中。图像以 100% 比例内嵌插入。

```csharp
public Shape InsertImage(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 包含图像的流。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将带有图像的形状从流插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    builder.Write("Image from stream: ");
    builder.InsertImage(stream);
}

doc.Save(ArtifactsDir + "Image.FromStream.docx");
```

演示如何将图像从流插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // 下面是从流中插入图像的三种方法。
    // 1 - 内联形状，其默认大小基于图像的原始尺寸：
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - 具有自定义尺寸的内联形状：
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - 具有自定义尺寸的浮动形状：
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(byte[]) {#insertimage}

将字节数组中的图像插入到文档中。图像以 100% 比例内嵌插入。

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | Byte[] | 包含图像的字节数组。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将图像从字节数组插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // 下面是从字节数组插入图像的三种方法。
    // 1 - 内联形状，其默认大小基于图像的原始尺寸：
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - 具有自定义尺寸的内联形状：
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - 具有自定义尺寸的浮动形状：
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

演示如何将图像从字节数组插入到文档中 (.NetStandard 2.0)。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 解码图像会将其转换为 .png 格式。
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // 下面是从字节数组插入图像的三种方法。
            // 1 - 内联形状，其默认大小基于图像的原始尺寸：
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - 具有自定义尺寸的内联形状：
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - 具有自定义尺寸的浮动形状：
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(Image, double, double) {#insertimage_5}

从 .NET 插入内嵌图像Image 对象放入文档中并将其缩放至指定大小。

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | Image | 要插入到文档中的图像。 |
| width | Double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将对象中的图像插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// 下面是从 Image 对象实例插入图像的三种方法。
// 1 - 内联形状，其默认大小基于图像的原始尺寸：
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - 具有自定义尺寸的内联形状：
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - 具有自定义尺寸的浮动形状：
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

演示如何将对象中的图像插入到文档中 (.NetStandard 2.0)。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 解码图像会将其转换为 .png 格式。
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // 下面是从 Image 对象实例插入图像的三种方法。
    // 1 - 内联形状，其默认大小基于图像的原始尺寸：
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - 具有自定义尺寸的内联形状：
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - 具有自定义尺寸的浮动形状：
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(string, double, double) {#insertimage_11}

将文件或 URL 中的内嵌图像插入到文档中，并将其缩放到指定的大小。

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 包含图像的文件。 |
| width | Double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将本地文件系统中的图像插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是从本地系统文件名插入图像的三种方法。
// 1 - 内联形状，其默认大小基于图像的原始尺寸：
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - 具有自定义尺寸的内联形状：
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - 具有自定义尺寸的浮动形状：
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(Stream, double, double) {#insertimage_8}

将内嵌图像从流插入到文档中并将其缩放到指定的大小。

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 包含图像的流。 |
| width | Double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将图像从流插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // 下面是从流中插入图像的三种方法。
    // 1 - 内联形状，其默认大小基于图像的原始尺寸：
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - 具有自定义尺寸的内联形状：
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - 具有自定义尺寸的浮动形状：
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(byte[], double, double) {#insertimage_2}

将字节数组中的内联图像插入到文档中并将其缩放到指定的大小。

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | Byte[] | 包含图像的字节数组。 |
| width | Double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将图像从字节数组插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // 下面是从字节数组插入图像的三种方法。
    // 1 - 内联形状，其默认大小基于图像的原始尺寸：
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - 具有自定义尺寸的内联形状：
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - 具有自定义尺寸的浮动形状：
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

演示如何将图像从字节数组插入到文档中 (.NetStandard 2.0)。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 解码图像会将其转换为 .png 格式。
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // 下面是从字节数组插入图像的三种方法。
            // 1 - 内联形状，其默认大小基于图像的原始尺寸：
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - 具有自定义尺寸的内联形状：
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - 具有自定义尺寸的浮动形状：
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(Image, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_4}

插入来自 .NET 的图像Image 指定位置和大小的对象。

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | Image | 要插入到文档中的图像。 |
| horzPos | RelativeHorizontalPosition | 指定从何处测量到图像的距离。 |
| left | Double | 从原点到图像左侧的距离（以点为单位）。 |
| vertPos | RelativeVerticalPosition | 指定从何处测量到图像的距离。 |
| top | Double | 从原点到图像顶部的距离（以点为单位）。 |
| width | Double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| wrapType | WrapType | 指定如何使文本环绕图像。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将对象中的图像插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// 下面是从 Image 对象实例插入图像的三种方法。
// 1 - 内联形状，其默认大小基于图像的原始尺寸：
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - 具有自定义尺寸的内联形状：
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - 具有自定义尺寸的浮动形状：
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

演示如何将对象中的图像插入到文档中 (.NetStandard 2.0)。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 解码图像会将其转换为 .png 格式。
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // 下面是从 Image 对象实例插入图像的三种方法。
    // 1 - 内联形状，其默认大小基于图像的原始尺寸：
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - 具有自定义尺寸的内联形状：
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - 具有自定义尺寸的浮动形状：
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_10}

在指定位置和大小插入文件或 URL 中的图像。

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 包含图像的文件。 |
| horzPos | RelativeHorizontalPosition | 指定从何处测量到图像的距离。 |
| left | Double | 从原点到图像左侧的距离（以点为单位）。 |
| vertPos | RelativeVerticalPosition | 指定从何处测量到图像的距离。 |
| top | Double | 从原点到图像顶部的距离（以点为单位）。 |
| width | Double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| wrapType | WrapType | 指定如何使文本环绕图像。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

展示如何插入图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 有两种方法可以使用文档生成器获取图像，然后将其作为浮动形状插入。
// 1 - 来自本地文件系统中的文件：
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - 来自 URL：
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

演示如何将图像从本地文件系统插入到文档中，同时保留其尺寸。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// InsertImage 方法创建一个浮动形状，其图像数据中包含传递的图像。
// 我们可以指定形状的尺寸，并将它们传递给此方法。
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// 传递负值作为预期尺寸将自动定义
// 形状的尺寸基于其图像的尺寸。
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

演示如何将本地文件系统中的图像插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是从本地系统文件名插入图像的三种方法。
// 1 - 内联形状，其默认大小基于图像的原始尺寸：
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - 具有自定义尺寸的内联形状：
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - 具有自定义尺寸的浮动形状：
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(Stream, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_7}

在指定位置和大小处插入流中的图像。

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 包含图像的流。 |
| horzPos | RelativeHorizontalPosition | 指定从何处测量到图像的距离。 |
| left | Double | 从原点到图像左侧的距离（以点为单位）。 |
| vertPos | RelativeVerticalPosition | 指定从何处测量到图像的距离。 |
| top | Double | 从原点到图像顶部的距离（以点为单位）。 |
| width | Double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| wrapType | WrapType | 指定如何使文本环绕图像。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将图像从流插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // 下面是从流中插入图像的三种方法。
    // 1 - 内联形状，其默认大小基于图像的原始尺寸：
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - 具有自定义尺寸的内联形状：
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - 具有自定义尺寸的浮动形状：
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertImage(byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertimage_1}

在指定位置和大小处插入字节数组中的图像。

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| imageBytes | Byte[] | 包含图像的字节数组。 |
| horzPos | RelativeHorizontalPosition | 指定从何处测量到图像的距离。 |
| left | Double | 从原点到图像左侧的距离（以点为单位）。 |
| vertPos | RelativeVerticalPosition | 指定从何处测量到图像的距离。 |
| top | Double | 从原点到图像顶部的距离（以点为单位）。 |
| width | Double | 图像的宽度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| wrapType | WrapType | 指定如何使文本环绕图像。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

### 例子

演示如何将图像从字节数组插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // 下面是从字节数组插入图像的三种方法。
    // 1 - 内联形状，其默认大小基于图像的原始尺寸：
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - 具有自定义尺寸的内联形状：
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - 具有自定义尺寸的浮动形状：
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

演示如何将图像从字节数组插入到文档中 (.NetStandard 2.0)。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 解码图像会将其转换为 .png 格式。
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // 下面是从字节数组插入图像的三种方法。
            // 1 - 内联形状，其默认大小基于图像的原始尺寸：
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - 具有自定义尺寸的内联形状：
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - 具有自定义尺寸的浮动形状：
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


