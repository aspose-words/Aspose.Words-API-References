---
title: ImageSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.save_format property. Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used"
type: docs
weight: 130
url: /it/python-net/aspose.words.saving/imagesaveoptions/save_format/
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
# Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
# modifica l'immagine mentre l'operazione di salvataggio la renderizza.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Possiamo regolare queste proprietà per modificare la luminosità e il contrasto dell'immagine.
# Entrambe sono su una scala da 0 a 1 e hanno valore predefinito di 0,5.
options.image_brightness = 0.3
options.image_contrast = 0.7
# Possiamo regolare la risoluzione orizzontale e verticale con queste proprietà.
# Ciò influenzerà le dimensioni dell'immagine.
# Il valore predefinito per queste proprietà è 96,0, per una risoluzione di 96 dpi.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# Possiamo ridimensionare l'immagine usando questa proprietà. Il valore predefinito è 1,0, per una scala del 100%.
# Possiamo usare questa proprietà per annullare qualsiasi variazione delle dimensioni dell'immagine che il cambiamento della risoluzione potrebbe causare.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

