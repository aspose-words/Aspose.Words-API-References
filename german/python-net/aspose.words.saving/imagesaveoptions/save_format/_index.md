---
title: ImageSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.save_format property. Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used"
type: docs
weight: 130
url: /de/python-net/aspose.words.saving/imagesaveoptions/save_format/
---

## ImageSaveOptions.save_format property

Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used.
Can be a raster
[SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP),
[SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG) or vector [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../../aspose.words/saveformat/#EPS),
[SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P), [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Remarks

The number of other options depends on the selected format.

Also, it is possible to save to SVG both via [ImageSaveOptions](../) and via [SvgSaveOptions](../../svgsaveoptions/).




### Examples

Shows how to edit the image while Aspose.Words converts a document to one.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben, um
# bearbeiten Sie das Bild, während der Speichervorgang es rendert.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Wir können diese Eigenschaften anpassen, um die Helligkeit und den Kontrast des Bildes zu ändern.
# Beide liegen auf einer Skala von 0‑1 und haben standardmäßig den Wert 0,5.
options.image_brightness = 0.3
options.image_contrast = 0.7
# Wir können die horizontale und vertikale Auflösung mit diesen Eigenschaften anpassen.
# Dies wird die Abmessungen des Bildes beeinflussen.
# Der Standardwert für diese Eigenschaften ist 96,0, für eine Auflösung von 96 dpi.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# Wir können das Bild mit dieser Eigenschaft skalieren. Der Standardwert ist 1,0, für eine Skalierung von 100 %.
# Wir können diese Eigenschaft verwenden, um Änderungen der Bildabmessungen, die durch eine Auflösungsänderung entstehen würden, zu neutralisieren.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

