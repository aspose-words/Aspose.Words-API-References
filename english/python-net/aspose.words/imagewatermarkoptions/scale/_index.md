---
title: ImageWatermarkOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageWatermarkOptions.scale property. Gets or sets the scale factor expressed as a fraction of the image"
type: docs
weight: 30
url: /python-net/aspose.words/imagewatermarkoptions/scale/
---

## ImageWatermarkOptions.scale property

Gets or sets the scale factor expressed as a fraction of the image. The default value is 0 - auto.


```python
@property
def scale(self) -> float:
    ...

@scale.setter
def scale(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

Valid values range from 0 to 65.5 inclusive.

Auto scale means that the watermark will be scaled to its max width and max height relative to
the page margins.




### See Also

* module [aspose.words](../../)
* class [ImageWatermarkOptions](../)

