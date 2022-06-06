---
title: InsertOnlineVideo
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 390
url: /net/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder.InsertOnlineVideo method (1 of 4)

Inserts an online video object into the document and scales it to the specified size.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | String | The URL to the video. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

Insertion of online video from the following resources is supported:

* https://www.youtube.com/
* https://vimeo.com/

If your online video is not displaying correctly, use [`InsertOnlineVideo`](../insertonlinevideo), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.

## Examples

Shows how to insert an online video into a document using a URL.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360, 270);

// We can watch the video from Microsoft Word by clicking on the shape.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertOnlineVideo method (2 of 4)

Inserts an online video object into the document and scales it to the specified size.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | String | The URL to the video. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | Double | Distance in points from the origin to the left side of the image. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | Double | Distance in points from the origin to the top side of the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | WrapType | Specifies how to wrap text around the image. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

Insertion of online video from the following resources is supported:

* https://www.youtube.com/
* https://vimeo.com/

If your online video is not displaying correctly, use [`InsertOnlineVideo`](../insertonlinevideo), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.

## Examples

Shows how to insert an online video into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Insert a shape that plays a video from the web when clicked in Microsoft Word.
// This rectangular shape will contain an image based on the first frame of the linked video
// and a "play button" visual prompt. The video has an aspect ratio of 16:9.
// We will set the shape's size to that ratio, so the image does not appear stretched.
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertOnlineVideo method (3 of 4)

Inserts an online video object into the document and scales it to the specified size.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | String | The URL to the video. |
| videoEmbedCode | String | The embed code for the video. |
| thumbnailImageBytes | Byte[] | The thumbnail image bytes. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

## Examples

Shows how to insert an online video into a document with a custom thumbnail.

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
        // Below are two ways of creating a shape with a custom thumbnail, which links to an online video
        // that will play when we click on the shape in Microsoft Word.
        // 1 -  Insert an inline shape at the builder's node insertion cursor:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 -  Insert a floating shape:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertOnlineVideo method (4 of 4)

Inserts an online video object into the document and scales it to the specified size.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | String | The URL to the video. |
| videoEmbedCode | String | The embed code for the video. |
| thumbnailImageBytes | Byte[] | The thumbnail image bytes. |
| horzPos | RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | Double | Distance in points from the origin to the left side of the image. |
| vertPos | RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | Double | Distance in points from the origin to the top side of the image. |
| width | Double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | Double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | WrapType | Specifies how to wrap text around the image. |

### Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

## Examples

Shows how to insert an online video into a document with a custom thumbnail.

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
        // Below are two ways of creating a shape with a custom thumbnail, which links to an online video
        // that will play when we click on the shape in Microsoft Word.
        // 1 -  Insert an inline shape at the builder's node insertion cursor:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 -  Insert a floating shape:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
