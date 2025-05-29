---
title: DocumentBuilder.InsertOnlineVideo
linktitle: InsertOnlineVideo
articleTitle: InsertOnlineVideo
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 的 InsertOnlineVideo 方法轻松地在文档中添加和缩放在线视频，以增强参与度和创造力。
type: docs
weight: 440
url: /zh/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo}

将在线视频对象插入文档并将其缩放到指定大小。

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
| width | Double | 图像的宽度（以磅为单位）。可以为负值或零，以请求 100% 缩放。 |
| height | Double | 图像的高度（以磅为单位）。可以为负值或零，以请求 100% 缩放。 |
| wrapType | WrapType | 指定如何让文本环绕图像。 |

### 返回值

刚刚插入的图像节点。

## 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)此方法返回的对象。

支持插入以下资源的在线视频：

* https://www.youtube.com/
* https://vimeo.com/

如果您的在线视频显示不正确，请使用`InsertOnlineVideo`，它接受自定义嵌入的 html 代码。

嵌入视频的代码可能因提供商而异，请咨询您选择的相应提供商以了解详细信息。

## 例子

展示如何将在线视频插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838”；

// 在 Microsoft Word 中插入一个形状，单击该形状即可播放来自网络的视频。
// 此矩形将包含基于链接视频第一帧的图像
// 以及“播放按钮”的视觉提示。视频的宽高比为 16:9。
// 我们将把形状的大小设置为该比例，这样图像就不会显得被拉伸。
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], double, double*) {#insertonlinevideo_3}

将在线视频对象插入文档并将其缩放到指定大小。

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | String | 视频的 URL。 |
| videoEmbedCode | String | 视频的嵌入代码。 |
| thumbnailImageBytes | Byte[] | 缩略图字节。 |
| width | Double | 图像的宽度（以磅为单位）。可以为负值或零，以请求 100% 缩放。 |
| height | Double | 图像的高度（以磅为单位）。可以为负值或零，以请求 100% 缩放。 |

### 返回值

刚刚插入的图像节点。

## 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)此方法返回的对象。

## 例子

展示如何将在线视频插入带有自定义缩略图的文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838”；
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" 宽度=\"640\" 高度=\"360\" 框架边框=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // 下面是两种创建带有自定义缩略图的形状的方法，该形状链接到在线视频
        // 当我们单击 Microsoft Word 中的形状时，它将播放。
        // 1 - 在构建器的节点插入光标处插入内联形状：
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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo_2}

将在线视频对象插入文档并将其缩放到指定大小。

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | String | 视频的 URL。 |
| videoEmbedCode | String | 视频的嵌入代码。 |
| thumbnailImageBytes | Byte[] | 缩略图字节。 |
| horzPos | RelativeHorizontalPosition | 指定从哪里测量到图像的距离。 |
| left | Double | 从原点到图像左侧的距离（以点为单位）。 |
| vertPos | RelativeVerticalPosition | 指定从哪里测量到图像的距离。 |
| top | Double | 从原点到图像顶部的距离（以点为单位）。 |
| width | Double | 图像的宽度（以磅为单位）。可以为负值或零，以请求 100% 缩放。 |
| height | Double | 图像的高度（以磅为单位）。可以为负值或零，以请求 100% 缩放。 |
| wrapType | WrapType | 指定如何让文本环绕图像。 |

### 返回值

刚刚插入的图像节点。

## 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)此方法返回的对象。

## 例子

展示如何将在线视频插入带有自定义缩略图的文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838”；
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" 宽度=\"640\" 高度=\"360\" 框架边框=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // 下面是两种创建带有自定义缩略图的形状的方法，该形状链接到在线视频
        // 当我们单击 Microsoft Word 中的形状时，它将播放。
        // 1 - 在构建器的节点插入光标处插入内联形状：
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

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, double, double*) {#insertonlinevideo_1}

将在线视频对象插入文档并将其缩放到指定大小。

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | String | 视频的 URL。 |
| width | Double | 图像的宽度（以磅为单位）。可以为负值或零，以请求 100% 缩放。 |
| height | Double | 图像的高度（以磅为单位）。可以为负值或零，以请求 100% 缩放。 |

### 返回值

刚刚插入的图像节点。

## 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)此方法返回的对象。

支持插入以下资源的在线视频：

* https://www.youtube.com/
* https://vimeo.com/

如果您的在线视频显示不正确，请使用`InsertOnlineVideo`，它接受自定义嵌入的 html 代码。

嵌入视频的代码可能因提供商而异，请咨询您选择的相应提供商以了解详细信息。

## 例子

展示如何使用 URL 将在线视频插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/g1N9ke8Prmk", 360, 270);

// 我们可以通过单击形状来观看来自 Microsoft Word 的视频。
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
