---
title: ShapeBase.bounds property
linktitle: bounds property
articleTitle: bounds property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds property. Gets or sets the location and size of the containing block of the shape."
type: docs
weight: 70
url: /tr/python-net/aspose.words.drawing/shapebase/bounds/
---

## ShapeBase.bounds property

Gets or sets the location and size of the containing block of the shape.


```python
@property
def bounds(self) -> aspose.pydrawing.RectangleF:
    ...

@bounds.setter
def bounds(self, value: aspose.pydrawing.RectangleF):
    ...

```

### Remarks

Ignores aspect ratio lock upon setting.


For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.




### Examples

Shows how to create and populate a group shape.

```python
doc = aw.Document()
# Bir grup şekli oluşturun. Grup şekli, çocuk şekil düğümlerinin bir koleksiyonunu görüntüleyebilir.
# Microsoft Word'de, grup şeklinin sınırları içinde veya grup şeklinin bir çocuk şekline tıklamak
# bu grup içindeki diğer tüm çocuk şekilleri seçer ve tüm şekilleri bir kerede ölçeklendirmemize ve taşımamıza izin verir.
group = aw.drawing.GroupShape(doc)
self.assertEqual(aw.drawing.WrapType.NONE, group.wrap_type)
# 400pt x 400pt boyutunda bir grup şekli oluşturun ve belge'nin yüzen şekil koordinat başlangıcına yerleştirin.
group.bounds = aspose.pydrawing.RectangleF(0, 0, 400, 400)
# Grubun iç koordinat düzlemi boyutunu 500 x 500pt olarak ayarlayın.
# Grubun sol üst köşesi (0, 0) x ve y koordinatına sahip olacaktır,
# ve sağ alt köşe (500, 500) x ve y koordinatına sahip olacaktır.
group.coord_size = aspose.pydrawing.Size(500, 500)
# Grubun sol üst köşesinin koordinatlarını (-250, -250) olarak ayarlayın.
# Grubun merkezi artık (0, 0) x ve y koordinat değerine sahip olacaktır,
# ve sağ alt köşe (250, 250) konumunda olacaktır.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
# Bu grup şeklinin sınırını gösterecek bir dikdörtgen oluşturun ve gruba ekleyin.
child1 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child1.width = group.coord_size.width
child1.height = group.coord_size.height
child1.left = group.coord_origin.x
child1.top = group.coord_origin.y
group.append_child(child1)
# Bir şekil bir grup şeklin parçası olduğunda, ona bir çocuk düğüm olarak erişebilir ve ardından değiştirebiliriz.
group.get_child(aw.NodeType.SHAPE, 0, True).as_shape().stroke.dash_style = aw.drawing.DashStyle.DASH
# Küçük bir kırmızı yıldız oluşturun ve gruba ekleyin.
# Şekli, grubun koordinat orijiniyle hizalayın, bunu merkeze taşıdık.
child2 = aw.drawing.Shape(doc, aw.drawing.ShapeType.STAR)
child2.width = 20
child2.height = 20
child2.left = -10
child2.top = -10
child2.fill_color = aspose.pydrawing.Color.red
group.append_child(child2)
# Bir dikdörtgen ekleyin ve ardından aynı konuma bir resimle biraz daha küçük bir dikdörtgen daha ekleyin.
# Gruba eklediğimiz daha yeni şekiller eski şekillerin üzerine biner. Açık mavi dikdörtgen kırmızı yıldızın bir kısmını örtüştürecek,
# ve ardından resimli şekil, açık mavi dikdörtgeni çerçeve olarak kullanarak onun üzerine biner.
# "ZOrder" özelliklerini kullanarak şekillerin bir grup şekil içindeki düzenini değiştiremeziz.
child3 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child3.width = 250
child3.height = 250
child3.left = -250
child3.top = -250
child3.fill_color = aspose.pydrawing.Color.light_blue
group.append_child(child3)
child4 = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
child4.width = 200
child4.height = 200
child4.left = -225
child4.top = -225
group.append_child(child4)
group.get_child(aw.NodeType.SHAPE, 3, True).as_shape().image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Grup şekline bir metin kutusu ekleyin. Metin kutusunun sağ kenarı "Left" özelliğiyle ayarlayın
# grup şeklinin sağ sınırına dokunsun. Metin kutusunun dışarıda durması için "Top" özelliğini ayarlayın
# grup şeklinin sınırına, üst kenarı grup şeklinin alt kenar boşluğuna hizalanacak şekilde.
child5 = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
child5.width = 200
child5.height = 50
child5.left = group.coord_size.width + group.coord_origin.x - 200
child5.top = group.coord_size.height + group.coord_origin.y
group.append_child(child5)
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(group)
builder.move_to(group.get_child(aw.NodeType.SHAPE, 4, True).as_shape().append_child(aw.Paragraph(doc)))
builder.write('Hello world!')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GroupShape.docx')
```

Shows how to verify shape containing block boundaries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.LINE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=50, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=50, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.stroke_color = aspose.pydrawing.Color.orange
# Satır kendisi belge sayfasında çok az yer kaplasa da,
# "Bounds" özelliklerini kullanarak boyutunu belirleyebileceğimiz dikdörtgen bir kapsayıcı blok işgal eder.
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)
# Bir grup şekil oluşturun ve ardından "Bounds" özelliğiyle kapsayıcı bloğunun boyutunu ayarlayın.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(0, 100, 250, 250)
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
# Bir dikdörtgen oluşturun, kapsama bloğunun boyutunu doğrulayın ve ardından grup şekline ekleyin.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
self.assertEqual(aspose.pydrawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)
group.append_child(shape)
# Grup şeklinin koordinat düzleminin orijini, kapsayıcı bloğunun sol üst köşesindedir,
# ve (1000, 1000) x ve y koordinatları sağ alt köşededir.
# Grup şeklimiz 250x250pt boyutunda, bu yüzden grup şeklinin koordinat düzlemindeki her 4pt
# belge gövdesinin koordinat düzleminde 1pt'ye karşılık gelir.
# Eklediğimiz her şekil de boyut olarak 4 kat küçülecek.
# Şeklin "BoundsInPoints" özelliğindeki değişiklik bunu yansıtacaktır.
self.assertEqual(aspose.pydrawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)
doc.first_section.body.first_paragraph.append_child(group)
# Bir şekil ekleyin ve onu grup şeklinin kapsayıcı bloğunun sınırlarının dışına yerleştirin.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000
group.append_child(shape)
# Grup şeklinin belge gövdesindeki ayak izi arttı, ancak kapsayıcı blok aynı kaldı.
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(aspose.pydrawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Bounds.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

