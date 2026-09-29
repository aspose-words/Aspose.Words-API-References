---
title: ImageBinarizationMethod enumeration
linktitle: ImageBinarizationMethod enumeration
articleTitle: ImageBinarizationMethod enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImageBinarizationMethod enumeration. Specifies the method used to binarize image."
type: docs
weight: 370
url: /tr/python-net/aspose.words.saving/imagebinarizationmethod/
---

## ImageBinarizationMethod enumeration

Specifies the method used to binarize image.


### Members

| Name | Description |
| --- | --- |
| THRESHOLD | Specifies threshold method. |
| FLOYD_STEINBERG_DITHERING | Specifies dithering using Floyd-Steinberg error diffusion method. |

### Examples

Shows how to set the TIFF binarization error threshold when using the Floyd-Steinberg method to render a TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Belgeyi TIFF olarak kaydettiğimizde, bir SaveOptions nesnesi geçirebiliriz
# Aspose.Words'ün bu görüntüyü işlerken uygulayacağı titreme (dithering) ayarını düzenlemek için.
# "ThresholdForFloydSteinbergDithering" özelliğinin varsayılan değeri 128'dir.
# Daha yüksek değerler genellikle daha koyu görüntüler üretir.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
options.tiff_compression = aw.saving.TiffCompression.CCITT3
options.tiff_binarization_method = aw.saving.ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING
options.threshold_for_floyd_steinberg_dithering = 240
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.FloydSteinbergDithering.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

