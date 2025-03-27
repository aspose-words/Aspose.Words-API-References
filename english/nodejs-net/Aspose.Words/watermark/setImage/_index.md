---
title: Watermark.setImage method
linktitle: setImage method
articleTitle: setImage method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Watermark.setImage method"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words/watermark/setImage/
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
setImage(image: Aspose.Words.JSImageoptions: Aspose.Words.ImageWatermarkOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | [JSImage](../../jsimage/) |  |
| options | [ImageWatermarkOptions](../../imagewatermarkoptions/) |  |

## setImage(imagePath, options) {#string_imagewatermarkoptions}

Adds Image watermark into the document.


```js
setImage(imagePath: stringoptions: Aspose.Words.ImageWatermarkOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imagePath | string | Path to the image file that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../imagewatermarkoptions/) | Defines additional options for the image watermark. |

### Remarks

If [ImageWatermarkOptions](../../imagewatermarkoptions/) is ``None``, the watermark will be set with default options.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws when the path is ``None``. |

## See Also

* module [Aspose.Words](../../)
* class [Watermark](../)

