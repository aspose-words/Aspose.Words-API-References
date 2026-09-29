---
title: ImageBinarizationMethod enumeration
linktitle: ImageBinarizationMethod enumeration
articleTitle: ImageBinarizationMethod enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImageBinarizationMethod enumeration. Specifies the method used to binarize image."
type: docs
weight: 370
url: /ru/python-net/aspose.words.saving/imagebinarizationmethod/
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

* module [aspose.words.saving](../)

