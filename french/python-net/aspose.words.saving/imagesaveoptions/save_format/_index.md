---
title: ImageSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.save_format property. Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used"
type: docs
weight: 130
url: /fr/python-net/aspose.words.saving/imagesaveoptions/save_format/
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

