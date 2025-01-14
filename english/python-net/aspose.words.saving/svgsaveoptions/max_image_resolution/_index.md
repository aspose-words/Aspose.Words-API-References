---
title: SvgSaveOptions.max_image_resolution property
linktitle: max_image_resolution property
articleTitle: max_image_resolution property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.max_image_resolution property. Gets or sets a value in pixels per inch that limits resolution of exported raster images"
type: docs
weight: 50
url: /python-net/aspose.words.saving/svgsaveoptions/max_image_resolution/
---

## SvgSaveOptions.max_image_resolution property

Gets or sets a value in pixels per inch that limits resolution of exported raster images. Default value is zero.


```python
@property
def max_image_resolution(self) -> int:
    ...

@max_image_resolution.setter
def max_image_resolution(self, value: int):
    ...

```

### Remarks

If the value of this property is non-zero, it limits resolution of exported raster images.
That is, higher-resolution images are resampled down to the limit and lower-resolution images are exported as is.

If the value of this property is zero, all raster images are exported without resampling.




### Examples

Shows how to set limit for image resolution.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.SvgSaveOptions()
save_options.max_image_resolution = 72
doc.save(file_name=ARTIFACTS_DIR + 'SvgSaveOptions.MaxImageResolution.svg', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SvgSaveOptions](../)

