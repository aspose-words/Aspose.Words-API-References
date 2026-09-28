---
title: ImageBinarizationMethod enumeration
linktitle: ImageBinarizationMethod enumeration
articleTitle: ImageBinarizationMethod enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImageBinarizationMethod enumeration. Specifies the method used to binarize image."
type: docs
weight: 370
url: /de/python-net/aspose.words.saving/imagebinarizationmethod/
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
# Wenn wir das Dokument als TIFF speichern, können wir ein SaveOptions‑Objekt übergeben, um
# das Dithering anzupassen, das Aspose.Words beim Rendern dieses Bildes anwenden wird.
# Der Standardwert der Eigenschaft "ThresholdForFloydSteinbergDithering" ist 128.
# Höhere Werte neigen dazu, dunklere Bilder zu erzeugen.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
options.tiff_compression = aw.saving.TiffCompression.CCITT3
options.tiff_binarization_method = aw.saving.ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING
options.threshold_for_floyd_steinberg_dithering = 240
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.FloydSteinbergDithering.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

