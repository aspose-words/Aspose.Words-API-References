---
title: HtmlSaveOptions.scale_image_to_shape_size property
linktitle: scale_image_to_shape_size property
articleTitle: scale_image_to_shape_size property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.scale_image_to_shape_size property. Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB"
type: docs
weight: 470
url: /tr/python-net/aspose.words.saving/htmlsaveoptions/scale_image_to_shape_size/
---

## HtmlSaveOptions.scale_image_to_shape_size property

Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML
or EPUB.
Default value is ``True``.



```python
@property
def scale_image_to_shape_size(self) -> bool:
    ...

@scale_image_to_shape_size.setter
def scale_image_to_shape_size(self, value: bool):
    ...

```

### Remarks

An image in a Microsoft Word document is a shape. The shape has a size and the image
has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels,
but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size.
The [HtmlSaveOptions.scale_image_to_shape_size](./) property controls where the scaling of the image
takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When [HtmlSaveOptions.scale_image_to_shape_size](./) is ``True``, the image is scaled by Aspose.Words
using high quality scaling during export to HTML. When [HtmlSaveOptions.scale_image_to_shape_size](./)
is ``False``, the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better
display quality in the browser and smaller file size when [HtmlSaveOptions.scale_image_to_shape_size](./) is ``True``,
but better printing quality and faster conversion when [HtmlSaveOptions.scale_image_to_shape_size](./) is ``False``.

In addition to shapes containing individual raster images, this option also affects group shapes consisting
of raster images. If [HtmlSaveOptions.scale_image_to_shape_size](./) is ``False`` and a group shape contains raster images
whose intrinsic resolution is higher than the value specified in [HtmlSaveOptions.image_resolution](../image_resolution/), Aspose.Words will
increase rendering resolution for that group. This allows to better preserve quality of grouped high resolution
images when saving to HTML.




### Examples

Shows how to disable the scaling of images to their parent shape dimensions when saving to .html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir görüntü içeren bir şekil ekleyin ve ardından bu şekli görüntüden oldukça daha küçük yapın.
image_shape = builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
image_shape.width = 50
image_shape.height = 50
# Görüntüler içeren şekiller içeren bir belgeyi HTML olarak kaydetmek, yerel dosya sisteminde bir görüntü dosyası oluşturur.
# her bir böyle şekil için. Çıktı HTML belgesi bu görüntülere bağlanmak ve göstermek için <image> etiketlerini kullanacaktır.
# Belgeyi HTML olarak kaydettiğimizde, belirlemek için bir SaveOptions nesnesi geçirebiliriz
# şekillerin içindeki tüm görüntülerin şekillerinin boyutlarına ölçeklenip ölçeklenmeyeceğini.
# "ScaleImageToShapeSize" bayrağını "true" olarak ayarlamak, her görüntüyü küçültecektir
# onu içeren şeklin boyutuna küçültecek, böylece kaydedilen görüntüler belgenin gerektirdiğinden daha büyük olmayacaktır.
# "ScaleImageToShapeSize" bayrağını "false" olarak ayarlamak, bu görüntülerin orijinal boyutlarını koruyacaktır,
# bu da görüntü kalitesini korumak karşılığında daha fazla yer kaplayacaktır.
options = aw.saving.HtmlSaveOptions()
options.scale_image_to_shape_size = scale_image_to_shape_size
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ScaleImageToShapeSize.html', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.image_resolution](../image_resolution/)

