---
title: ImageSaveOptions.tiff_binarization_method property
linktitle: tiff_binarization_method property
articleTitle: tiff_binarization_method property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.tiff_binarization_method property. Gets or sets method used while converting images to 1 bpp format when [ImageSaveOptions.save_format](../save_format/) is [SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF) and [ImageSaveOptions.tiff_compression](../tiff_compression/) is equal to [TiffCompression.CCITT3](../../tiffcompression/#CCITT3) or [TiffCompression.CCITT4](../../tiffcompression/#CCITT4)."
type: docs
weight: 160
url: /ru/python-net/aspose.words.saving/imagesaveoptions/tiff_binarization_method/
---

## ImageSaveOptions.tiff_binarization_method property

Gets or sets method used while converting images to 1 bpp format
when [ImageSaveOptions.save_format](../save_format/) is [SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF) and
[ImageSaveOptions.tiff_compression](../tiff_compression/) is equal to [TiffCompression.CCITT3](../../tiffcompression/#CCITT3) or [TiffCompression.CCITT4](../../tiffcompression/#CCITT4).



```python
@property
def tiff_binarization_method(self) -> aspose.words.saving.ImageBinarizationMethod:
    ...

@tiff_binarization_method.setter
def tiff_binarization_method(self, value: aspose.words.saving.ImageBinarizationMethod):
    ...

```

### Remarks

The default value is [ImageBinarizationMethod.THRESHOLD](../../imagebinarizationmethod/#THRESHOLD).




### Examples

Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Когда мы сохраняем документ в формате TIFF, мы можем передать объект SaveOptions, чтобы
# отрегулировать дизеринг, который Aspose.Words применит при рендеринге этого изображения.
# Значение свойства "ThresholdForFloydSteinbergDithering" по умолчанию равно 128.
# Более высокие значения, как правило, дают более тёмные изображения.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
options.tiff_compression = aw.saving.TiffCompression.CCITT3
options.tiff_binarization_method = aw.saving.ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING
options.threshold_for_floyd_steinberg_dithering = 240
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.FloydSteinbergDithering.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

