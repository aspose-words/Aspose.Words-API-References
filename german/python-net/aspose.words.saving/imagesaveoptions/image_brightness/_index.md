---
title: ImageSaveOptions.image_brightness property
linktitle: image_brightness property
articleTitle: image_brightness property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.image_brightness property. Gets or sets the brightness for the generated images."
type: docs
weight: 30
url: /de/python-net/aspose.words.saving/imagesaveoptions/image_brightness/
---

## ImageSaveOptions.image_brightness property

Gets or sets the brightness for the generated images.


```python
@property
def image_brightness(self) -> float:
    ...

@image_brightness.setter
def image_brightness(self, value: float):
    ...

```

### Remarks

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.




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

