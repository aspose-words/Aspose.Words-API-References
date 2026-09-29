---
title: ImageSaveOptions.horizontal_resolution property
linktitle: horizontal_resolution property
articleTitle: horizontal_resolution property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.horizontal_resolution property. Gets or sets the horizontal resolution for the generated images, in dots per inch."
type: docs
weight: 20
url: /sv/python-net/aspose.words.saving/imagesaveoptions/horizontal_resolution/
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

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

