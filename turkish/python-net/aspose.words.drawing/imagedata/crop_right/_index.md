---
title: ImageData.crop_right property
linktitle: crop_right property
articleTitle: crop_right property
second_title: Aspose.Words for Python
description: "ImageData.crop_right property. Defines the fraction of picture removal from the right side."
type: docs
weight: 80
url: /tr/python-net/aspose.words.drawing/imagedata/crop_right/
---

## ImageData.crop_right property

Defines the fraction of picture removal from the right side.


```python
@property
def crop_right(self) -> float:
    ...

@crop_right.setter
def crop_right(self, value: float):
    ...

```

### Remarks

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note 
that a value of 1 will display no picture at all. Negative values will result in 
the picture being squeezed inward from the edge being cropped (the empty space 
between the picture and the cropped edge will be filled by the fill color of the 
shape). Positive values less than 1 will result in the remaining picture being 
stretched to fit the shape.

The default value is 0.




### Examples

Shows how to edit a shape's image data.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
source_shape = img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
dst_doc = aw.Document()
# Kaynak belgeden bir şekil içe aktarın ve bunu ilk paragrafın sonuna ekleyin.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
# İçe aktarılan şekil bir görüntü içerir. Görüntünün özelliklerine ve ham verilerine ImageData nesnesi aracılığıyla erişebiliriz.
image_data = imported_shape.image_data
image_data.title = 'Imported Image'
self.assertTrue(image_data.has_image)
# Bir görüntünün kenarlığı yoksa, ImageData nesnesi kenarlık rengini boş olarak tanımlar.
self.assertEqual(4, image_data.borders.count)
self.assertEqual(aspose.pydrawing.Color.empty(), image_data.borders[0].color)
# Bu görüntü, yerel dosya sistemindeki başka bir şekle veya görüntü dosyasına bağlanmaz.
self.assertFalse(image_data.is_link)
self.assertFalse(image_data.is_link_only)
# "Brightness" ve "Contrast" özellikleri görüntünün parlaklığını ve kontrastını tanımlar
# 0-1 ölçeğinde, varsayılan değer 0.5'tedir.
image_data.brightness = 0.8
image_data.contrast = 1
# Yukarıdaki parlaklık ve kontrast değerleri, çok beyaz bir görüntü oluşturdu.
# Şeffaflıkla değiştirmek için, örneğin beyaz, ChromaKey özelliğiyle bir renk seçebiliriz.
image_data.chroma_key = aspose.pydrawing.Color.white
# Kaynak şekli tekrar içe aktarın ve görüntüyü tek renkli (monochrome) olarak ayarlayın.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.gray_scale = True
# Kaynak şekli tekrar içe aktararak üçüncü bir görüntü oluşturun ve onu BiLevel olarak ayarlayın.
# BiLevel, her pikseli orijinal renge daha yakın olan siyah ya da beyaz olarak ayarlar.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.bi_level = True
# Kırpma, 0-1 ölçeğinde belirlenir. Bir kenarı 0.3 oranında kırpma
# kırpılan kenarda görüntünün %30'unu kırpar.
imported_shape.image_data.crop_bottom = 0.3
imported_shape.image_data.crop_left = 0.3
imported_shape.image_data.crop_top = 0.3
imported_shape.image_data.crop_right = 0.3
dst_doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageData.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

