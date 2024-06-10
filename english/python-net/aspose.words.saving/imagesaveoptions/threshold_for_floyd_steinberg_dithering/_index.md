---
title: ImageSaveOptions.threshold_for_floyd_steinberg_dithering property
linktitle: threshold_for_floyd_steinberg_dithering property
articleTitle: threshold_for_floyd_steinberg_dithering property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.threshold_for_floyd_steinberg_dithering property. Gets or sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method"
type: docs
weight: 140
url: /python-net/aspose.words.saving/imagesaveoptions/threshold_for_floyd_steinberg_dithering/
---

## ImageSaveOptions.threshold_for_floyd_steinberg_dithering property

Gets or sets the threshold that determines the value
of the binarization error in the Floyd-Steinberg method.
when [ImageBinarizationMethod](../../imagebinarizationmethod/) is [ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING](../../imagebinarizationmethod/#FLOYD_STEINBERG_DITHERING).



```python
@property
def threshold_for_floyd_steinberg_dithering(self) -> int:
    ...

@threshold_for_floyd_steinberg_dithering.setter
def threshold_for_floyd_steinberg_dithering(self, value: int):
    ...

```

### Remarks

The default value is 128.




### Examples

Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(IMAGE_DIR + 'Logo.jpg')
# When we save the document as a TIFF, we can pass a SaveOptions object to
# adjust the dithering that Aspose.Words will apply when rendering this image.
# The default value of the "threshold_for_floyd_steinberg_dithering" property is 128.
# Higher values tend to produce darker images.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
options.tiff_compression = aw.saving.TiffCompression.CCITT3
options.tiff_binarization_method = aw.saving.ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING
options.threshold_for_floyd_steinberg_dithering = 240
doc.save(ARTIFACTS_DIR + 'ImageSaveOptions.floyd_steinberg_dithering.tiff', options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

