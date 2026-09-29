---
title: ImageSaveOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.scale property. Gets or sets the zoom factor for the generated images."
type: docs
weight: 140
url: /tr/python-net/aspose.words.saving/imagesaveoptions/scale/
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
# Belgeyi bir görüntü olarak kaydettiğimizde, bir SaveOptions nesnesi geçirebiliriz
# Kaydetme işlemi görüntüyü render ederken resmi düzenleyin.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Bu özellikleri görüntünün parlaklığını ve kontrastını değiştirmek için ayarlayabiliriz.
# İkisi de 0-1 ölçeğinde ve varsayılan olarak 0.5'tedir.
options.image_brightness = 0.3
options.image_contrast = 0.7
# Bu özelliklerle yatay ve dikey çözünürlüğü ayarlayabiliriz.
# Bu, görüntünün boyutlarını etkileyecek.
# Bu özelliklerin varsayılan değeri 96.0'dır, 96dpi çözünürlük için.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# Bu özelliği kullanarak görüntüyü ölçeklendirebiliriz. Varsayılan değer %100 ölçekleme için 1.0'dır.
# Çözünürlüğü değiştirmenin neden olacağı görüntü boyutlarındaki değişiklikleri iptal etmek için bu özelliği kullanabiliriz.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

Shows how to render an Office Math object into an image file in the local file system.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# "ImageSaveOptions" nesnesi oluştur, düğüm renderlayıcısının "Save" metoduna geçmek ve değiştirmek için.
# OfficeMath düğümünü bir görüntüye nasıl renderladığını.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# "Scale" özelliğini 5 olarak ayarla, nesneyi orijinal boyutunun beş katına renderlemek için.
save_options.scale = 5
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'Shape.RenderOfficeMath.png', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

