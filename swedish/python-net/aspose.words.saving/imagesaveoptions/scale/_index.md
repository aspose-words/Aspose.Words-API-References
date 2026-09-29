---
title: ImageSaveOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.scale property. Gets or sets the zoom factor for the generated images."
type: docs
weight: 140
url: /sv/python-net/aspose.words.saving/imagesaveoptions/scale/
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
# När vi sparar dokumentet som en bild kan vi skicka ett SaveOptions-objekt till
# redigera bilden medan sparningsoperationen renderar den.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Vi kan justera dessa egenskaper för att ändra bildens ljusstyrka och kontrast.
# Båda är på en skala från 0 till 1 och har standardvärdet 0,5.
options.image_brightness = 0.3
options.image_contrast = 0.7
# Vi kan justera horisontell och vertikal upplösning med dessa egenskaper.
# Detta kommer att påverka bildens dimensioner.
# Standardvärdet för dessa egenskaper är 96,0 för en upplösning på 96 dpi.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# Vi kan skala bilden med denna egenskap. Standardvärdet är 1,0 för en skalning på 100 %.
# Vi kan använda denna egenskap för att motverka eventuella förändringar i bildens dimensioner som en ändring av upplösningen skulle orsaka.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

Shows how to render an Office Math object into an image file in the local file system.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# Skapa ett "ImageSaveOptions"-objekt för att skicka till nodrenderarens "Save"-metod för att modifiera
# hur den renderar OfficeMath-noden till en bild.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Ange egenskapen "Scale" till 5 för att rendera objektet till fem gånger dess ursprungliga storlek.
save_options.scale = 5
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'Shape.RenderOfficeMath.png', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

