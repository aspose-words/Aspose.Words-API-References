---
title: ImageSaveOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.scale property. Gets or sets the zoom factor for the generated images."
type: docs
weight: 140
url: /it/python-net/aspose.words.saving/imagesaveoptions/scale/
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

Shows how to render an Office Math object into an image file in the local file system.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# Crea un oggetto "ImageSaveOptions" da passare al metodo "Save" del renderer dei nodi per modificare
# come rende il nodo OfficeMath in un'immagine.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Imposta la proprietà "Scale" a 5 per rendere l'oggetto cinque volte più grande della sua dimensione originale.
save_options.scale = 5
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'Shape.RenderOfficeMath.png', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

