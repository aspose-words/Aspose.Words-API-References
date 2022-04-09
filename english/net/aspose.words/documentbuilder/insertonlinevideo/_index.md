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

| parameter | description |
| --- | --- |
| videoUrl | The URL to the video. |
| width | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | The height of the image in points. Can be a negative or zero value to request 100% scale. |

## Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

Insertion of online video from the following resources is supported:

* https://www.youtube.com/
* https://vimeo.com/

If your online video is not displaying correctly, use [`InsertOnlineVideo`](../insertonlinevideo), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertOnlineVideo method (2 of 4)

Inserts an online video object into the document and scales it to the specified size.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| parameter | description |
| --- | --- |
| videoUrl | The URL to the video. |
| videoEmbedCode | The embed code for the video. |
| thumbnailImageBytes | The thumbnail image bytes. |
| width | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | The height of the image in points. Can be a negative or zero value to request 100% scale. |

## Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

---

## DocumentBuilder.InsertOnlineVideo method (3 of 4)

Inserts an online video object into the document and scales it to the specified size.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| parameter | description |
| --- | --- |
| videoUrl | The URL to the video. |
| horzPos | Specifies where the distance to the image is measured from. |
| left | Distance in points from the origin to the left side of the image. |
| vertPos | Specifies where the distance to the image measured from. |
| top | Distance in points from the origin to the top side of the image. |
| width | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | Specifies how to wrap text around the image. |

## Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

Insertion of online video from the following resources is supported:

* https://www.youtube.com/
* https://vimeo.com/

If your online video is not displaying correctly, use [`InsertOnlineVideo`](../insertonlinevideo), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
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

| parameter | description |
| --- | --- |
| videoUrl | The URL to the video. |
| videoEmbedCode | The embed code for the video. |
| thumbnailImageBytes | The thumbnail image bytes. |
| horzPos | Specifies where the distance to the image is measured from. |
| left | Distance in points from the origin to the left side of the image. |
| vertPos | Specifies where the distance to the image measured from. |
| top | Distance in points from the origin to the top side of the image. |
| width | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | Specifies how to wrap text around the image. |

## Return Value

The image node that was just inserted.

## Remarks

You can change the image size, location, positioning method and other settings using the [`Shape`](../../../aspose.words.drawing/shape) object returned by this method.

### See Also

* class [Shape](../../../aspose.words.drawing/shape)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition)
* enum [WrapType](../../../aspose.words.drawing/wraptype)
* class [DocumentBuilder](../../documentbuilder)
* namespace [Aspose.Words](../../documentbuilder)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
