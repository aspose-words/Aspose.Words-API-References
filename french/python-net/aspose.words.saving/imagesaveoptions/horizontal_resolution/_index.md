---
title: ImageSaveOptions.horizontal_resolution property
linktitle: horizontal_resolution property
articleTitle: horizontal_resolution property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.horizontal_resolution property. Gets or sets the horizontal resolution for the generated images, in dots per inch."
type: docs
weight: 20
url: /fr/python-net/aspose.words.saving/imagesaveoptions/horizontal_resolution/
---

## ImageSaveOptions.horizontal_resolution property

Gets or sets the horizontal resolution for the generated images, in dots per inch.


```python
@property
def horizontal_resolution(self) -> float:
    ...

@horizontal_resolution.setter
def horizontal_resolution(self, value: float):
    ...

```

### Remarks

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.




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

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

