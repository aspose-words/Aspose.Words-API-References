---
title: ImageSaveOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.scale property. Gets or sets the zoom factor for the generated images."
type: docs
weight: 140
url: /de/python-net/aspose.words.saving/imagesaveoptions/scale/
---

## ImageSaveOptions.scale property

Gets or sets the zoom factor for the generated images.


```python
@property
def scale(self) -> float:
    ...

@scale.setter
def scale(self, value: float):
    ...

```

### Remarks

The default value is 1.0. The value must be greater than 0.


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

Shows how to render an Office Math object into an image file in the local file system.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# Erstelle ein "ImageSaveOptions"-Objekt, um es an die "Save"-Methode des Node-Renderers zu übergeben, um zu ändern
# wie es den OfficeMath-Knoten in ein Bild rendert.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Setze die Eigenschaft "Scale" auf 5, um das Objekt fünfmal so groß wie die Originalgröße zu rendern.
save_options.scale = 5
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'Shape.RenderOfficeMath.png', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

