---
title: Watermark.setImage method
linktitle: setImage method
articleTitle: setImage method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Watermark.setImage method"
type: docs
weight: 30
url: /nodejs-net/aspose.words/watermark/setImage/
---

## setImage(image) {#jsimage}

```js
setImage(image: Aspose.Words.JSImage)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | [JSImage](../../jsimage/) |  |

## setImage(image, options) {#jsimage_imagewatermarkoptions}

```js
setImage(image: Aspose.Words.JSImage, options: Aspose.Words.ImageWatermarkOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | [JSImage](../../jsimage/) |  |
| options | [ImageWatermarkOptions](../../imagewatermarkoptions/) |  |

## setImage(imagePath, options) {#string_imagewatermarkoptions}

Adds Image watermark into the document.


```js
setImage(imagePath: string, options: Aspose.Words.ImageWatermarkOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imagePath | string | Path to the image file that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../imagewatermarkoptions/) | Defines additional options for the image watermark. |

### Remarks

If [ImageWatermarkOptions](../../imagewatermarkoptions/) is ``null``, the watermark will be set with default options.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws when the path is ``null``. |

## setImage(imageStream, options) {#buffer_imagewatermarkoptions}

Adds Image watermark into the document.


```js
setImage(imageStream: Buffer, options: Aspose.Words.ImageWatermarkOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageStream | Buffer | The stream containing the image data that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../imagewatermarkoptions/) | Defines additional options for the image watermark. |

### Remarks

If [ImageWatermarkOptions](../../imagewatermarkoptions/) is ``null``, the watermark will be set with default options.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws when the path is ``null``. |

## See Also

* module [Aspose.Words](../../)
* class [Watermark](../)

