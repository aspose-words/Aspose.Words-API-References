---
title: InsertOnlineVideo
second_title: Aspose.Words for .NET API 参考
description: 将在线视频对象插入到文档中并缩放到指定大小
type: docs
weight: 390
url: /zh/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(string, double, double) {#insertonlinevideo_1}

将在线视频对象插入到文档中并缩放到指定大小。

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | String | 视频的 URL。 |
| width | Double | 图像的宽度，以磅为单位。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 :::更改图像大小、位置、定位方法和其他设置R5:T:Aspose.Words.Drawing.Shape:::此方法返回的对象。

支持从以下资源插入在线视频:

* https://www.youtube.com/
* https://vimeo.com/

如果您的在线视频未显示正确地，使用[`InsertOnlineVideo`](../insertonlinevideo)，它接受自定义嵌入的 html 代码.

嵌入视频的代码可能因供应商而异，详情请咨询您选择的相应供应商。

### 例子

展示如何使用 URL 将在线视频插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360, 270);

// 我们可以通过单击形状来观看 Microsoft Word 中的视频。
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* 命名空间 [Aspose.Words](../../documentbuilder)
* 部件 [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo}

将在线视频对象插入到文档中并缩放到指定大小。

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | String | 视频的 URL。 |
| horzPos | RelativeHorizontalPosition | 指定从哪里测量到图像的距离。 |
| left | Double | 从原点到图像左侧的距离（以点为单位）。 |
| vertPos | RelativeVerticalPosition | 指定从哪里测量到图像的距离。 |
| top | Double | 从原点到图像顶部的距离（以点为单位）。 |
| width | Double | 图像的宽度，以磅为单位。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| wrapType | WrapType | 指定如何在图像周围环绕文本。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 :::更改图像大小、位置、定位方法和其他设置R5:T:Aspose.Words.Drawing.Shape:::此方法返回的对象。

支持从以下资源插入在线视频:

* https://www.youtube.com/
* https://vimeo.com/

如果您的在线视频未显示正确地，使用[`InsertOnlineVideo`](../insertonlinevideo)，它接受自定义嵌入的 html 代码.

嵌入视频的代码可能因供应商而异，详情请咨询您选择的相应供应商。

### 例子

显示如何将在线视频插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// 在 Microsoft Word 中单击时插入一个播放网络视频的形状。
// 这个矩形将包含基于链接视频的第一帧的图像
// 和“播放按钮”视觉提示。该视频的宽高比为 16:9。
// 我们将形状的大小设置为该比例，因此图像不会出现拉伸。
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* 命名空间 [Aspose.Words](../../documentbuilder)
* 部件 [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], double, double) {#insertonlinevideo_3}

将在线视频对象插入到文档中并缩放到指定大小。

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | String | 视频的 URL。 |
| videoEmbedCode | String | 视频的嵌入代码。 |
| thumbnailImageBytes | Byte[] | 缩略图图像字节。 |
| width | Double | 图像的宽度，以磅为单位。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 :::更改图像大小、位置、定位方法和其他设置R5:T:Aspose.Words.Drawing.Shape:::此方法返回的对象。

### 例子

展示如何使用自定义缩略图将在线视频插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // 下面是使用自定义缩略图创建形状的两种方法，链接到在线视频
        // 当我们在 Microsoft Word 中单击形状时将播放。
        // 1 - 在构建器的节点插入光标处插入一个内联形状：
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - 插入浮动形状：
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* 命名空间 [Aspose.Words](../../documentbuilder)
* 部件 [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo_2}

将在线视频对象插入到文档中并缩放到指定大小。

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | String | 视频的 URL。 |
| videoEmbedCode | String | 视频的嵌入代码。 |
| thumbnailImageBytes | Byte[] | 缩略图图像字节。 |
| horzPos | RelativeHorizontalPosition | 指定从哪里测量到图像的距离。 |
| left | Double | 从原点到图像左侧的距离（以点为单位）。 |
| vertPos | RelativeVerticalPosition | 指定从哪里测量到图像的距离。 |
| top | Double | 从原点到图像顶部的距离（以点为单位）。 |
| width | Double | 图像的宽度，以磅为单位。可以是负值或零值以请求 100% 比例。 |
| height | Double | 图像的高度（以磅为单位）。可以是负值或零值以请求 100% 比例。 |
| wrapType | WrapType | 指定如何在图像周围环绕文本。 |

### 返回值

刚刚插入的图像节点。

### 评论

您可以使用 :::更改图像大小、位置、定位方法和其他设置R5:T:Aspose.Words.Drawing.Shape:::此方法返回的对象。

### 例子

展示如何使用自定义缩略图将在线视频插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // 下面是使用自定义缩略图创建形状的两种方法，链接到在线视频
        // 当我们在 Microsoft Word 中单击形状时将播放。
        // 1 - 在构建器的节点插入光标处插入一个内联形状：
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - 插入浮动形状：
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* 命名空间 [Aspose.Words](../../documentbuilder)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
