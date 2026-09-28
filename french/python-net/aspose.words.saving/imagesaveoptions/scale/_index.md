---
title: ImageSaveOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.scale property. Gets or sets the zoom factor for the generated images."
type: docs
weight: 140
url: /fr/python-net/aspose.words.saving/imagesaveoptions/scale/
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
# Lorsque nous enregistrons le document en tant qu'image, nous pouvons passer un objet SaveOptions à
# modifiez l'image pendant que l'opération d'enregistrement la rend.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Nous pouvons ajuster ces propriétés pour modifier la luminosité et le contraste de l'image.
# Les deux sont sur une échelle de 0 à 1 et sont à 0,5 par défaut.
options.image_brightness = 0.3
options.image_contrast = 0.7
# Nous pouvons ajuster la résolution horizontale et verticale avec ces propriétés.
# Cela affectera les dimensions de l'image.
# La valeur par défaut de ces propriétés est 96,0, pour une résolution de 96 dpi.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# Nous pouvons mettre à l'échelle l'image en utilisant cette propriété. La valeur par défaut est 1,0, pour un agrandissement de 100 %.
# Nous pouvons utiliser cette propriété pour annuler toute modification des dimensions de l'image que le changement de résolution pourrait entraîner.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

Shows how to render an Office Math object into an image file in the local file system.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# Créez un objet "ImageSaveOptions" à transmettre à la méthode "Save" du rendu de nœud pour modifier
# la façon dont il rend le nœud OfficeMath en image.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Définissez la propriété "Scale" à 5 pour rendre l'objet cinq fois plus grand que sa taille originale.
save_options.scale = 5
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'Shape.RenderOfficeMath.png', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

