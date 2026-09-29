---
title: ImageSaveOptions.image_contrast property
linktitle: image_contrast property
articleTitle: image_contrast property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.image_contrast property. Gets or sets the contrast for the generated images."
type: docs
weight: 50
url: /it/python-net/aspose.words.saving/imagesaveoptions/image_contrast/
---

## ImageSaveOptions.image_contrast property

Gets or sets the contrast for the generated images.


```python
@property
def image_contrast(self) -> float:
    ...

@image_contrast.setter
def image_contrast(self, value: float):
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

