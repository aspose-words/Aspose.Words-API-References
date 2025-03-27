---
title: DocumentBuilder.insertOnlineVideo method
linktitle: insertOnlineVideo method
articleTitle: insertOnlineVideo method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.insertOnlineVideo method"
type: docs
weight: 440
url: /nodejs-net/Aspose.Words/documentbuilder/insertOnlineVideo/
---

## insertOnlineVideo(videoUrl, width, height) {#string_number_number}

Inserts an online video object into the document and scales it to the specified size.


```js
insertOnlineVideo(videoUrl: stringwidth: numberheight: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | string | The URL to the video. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../Aspose.Words.Drawing/shape/) object returned by this method.

Insertion of online video from the following resources is supported:


* https://www.youtube.com/
  
* https://vimeo.com/
  
If your online video is not displaying correctly, use [DocumentBuilder.insertOnlineVideo()](./#string_string_number[]_number_number), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.




### Returns

The image node that was just inserted.


## insertOnlineVideo(videoUrl, horzPos, left, vertPos, top, width, height, wrapType) {#string_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype}

Inserts an online video object into the document and scales it to the specified size.


```js
insertOnlineVideo(videoUrl: stringhorzPos: Aspose.Words.Drawing.RelativeHorizontalPositionleft: numbervertPos: Aspose.Words.Drawing.RelativeVerticalPositiontop: numberwidth: numberheight: numberwrapType: Aspose.Words.Drawing.WrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | string | The URL to the video. |
| horzPos | [RelativeHorizontalPosition](../../../Aspose.Words.Drawing/relativehorizontalposition/) | Specifies where the distance to the image is measured from. |
| left | number | Distance in points from the origin to the left side of the image. |
| vertPos | [RelativeVerticalPosition](../../../Aspose.Words.Drawing/relativeverticalposition/) | Specifies where the distance to the image measured from. |
| top | number | Distance in points from the origin to the top side of the image. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | [WrapType](../../../Aspose.Words.Drawing/wraptype/) | Specifies how to wrap text around the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../Aspose.Words.Drawing/shape/) object returned by this method.

Insertion of online video from the following resources is supported:


* https://www.youtube.com/
  
* https://vimeo.com/
  
If your online video is not displaying correctly, use [DocumentBuilder.insertOnlineVideo()](./#string_string_number[]_number_number), which accepts custom embedded html code.

The code for embedding video can vary between providers, consult your corresponding provider of choice for details.




### Returns

The image node that was just inserted.


## insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, width, height) {#string_string_number[]_number_number}

Inserts an online video object into the document and scales it to the specified size.


```js
insertOnlineVideo(videoUrl: stringvideoEmbedCode: stringthumbnailImageBytes: number[]width: numberheight: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | string | The URL to the video. |
| videoEmbedCode | string | The embed code for the video. |
| thumbnailImageBytes | number[] | The thumbnail image bytes. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../Aspose.Words.Drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, horzPos, left, vertPos, top, width, height, wrapType) {#string_string_number[]_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype}

Inserts an online video object into the document and scales it to the specified size.


```js
insertOnlineVideo(videoUrl: stringvideoEmbedCode: stringthumbnailImageBytes: number[]horzPos: Aspose.Words.Drawing.RelativeHorizontalPositionleft: numbervertPos: Aspose.Words.Drawing.RelativeVerticalPositiontop: numberwidth: numberheight: numberwrapType: Aspose.Words.Drawing.WrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| videoUrl | string | The URL to the video. |
| videoEmbedCode | string | The embed code for the video. |
| thumbnailImageBytes | number[] | The thumbnail image bytes. |
| horzPos | [RelativeHorizontalPosition](../../../Aspose.Words.Drawing/relativehorizontalposition/) | Specifies where the distance to the image is measured from. |
| left | number | Distance in points from the origin to the left side of the image. |
| vertPos | [RelativeVerticalPosition](../../../Aspose.Words.Drawing/relativeverticalposition/) | Specifies where the distance to the image measured from. |
| top | number | Distance in points from the origin to the top side of the image. |
| width | number | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | number | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | [WrapType](../../../Aspose.Words.Drawing/wraptype/) | Specifies how to wrap text around the image. |

### Remarks

You can change the image size, location, positioning method and other settings using the 
[Shape](../../../Aspose.Words.Drawing/shape/) object returned by this method.




### Returns

The image node that was just inserted.


## Examples

Shows how to insert an online video into a document using a URL.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertOnlineVideo("https://youtu.be/g1N9ke8Prmk", 360, 270);

// We can watch the video from Microsoft Word by clicking on the shape.
doc.save(base.artifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

Shows how to insert an online video into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let videoUrl = "https://vimeo.com/52477838";

// Insert a shape that plays a video from the web when clicked in Microsoft Word.
// This rectangular shape will contain an image based on the first frame of the linked video
// and a "play button" visual prompt. The video has an aspect ratio of 16:9.
// We will set the shape's size to that ratio, so the image does not appear stretched.
builder.insertOnlineVideo(videoUrl, aw.Drawing.RelativeHorizontalPosition.LeftMargin, 0,
  aw.Drawing.RelativeVerticalPosition.TopMargin, 0, 320, 180, aw.Drawing.WrapType.Square);

doc.save(base.artifactsDir + "DocumentBuilder.insertOnlineVideo.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

