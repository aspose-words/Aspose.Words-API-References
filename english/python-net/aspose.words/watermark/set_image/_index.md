---
title: Watermark.set_image method
linktitle: set_image method
articleTitle: set_image method
second_title: Aspose.Words for Python
description: "Watermark.set_image method. Adds Image watermark into the document."
type: docs
weight: 30
url: /python-net/aspose.words/watermark/set_image/
---

## set_image(image_path, options) {#str_imagewatermarkoptions}

Adds Image watermark into the document.


```python
def set_image(self, image_path: str, options: aspose.words.ImageWatermarkOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| image_path | str | Path to the image file that is displayed as a watermark. |
| options | [ImageWatermarkOptions](../../imagewatermarkoptions/) | Defines additional options for the image watermark. |

### Remarks

If [ImageWatermarkOptions](../../imagewatermarkoptions/) is ``None``, the watermark will be set with default options.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentNullException)) | Throws when the path is ``None``. |

### See Also

* module [aspose.words](../../)
* class [Watermark](../)

