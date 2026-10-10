---
title: ShapeBase.coord_size property
linktitle: coord_size property
articleTitle: coord_size property
second_title: Aspose.Words for Python
description: "ShapeBase.coord_size property. The width and height of the coordinate space inside the containing block of this shape."
type: docs
weight: 120
url: /tr/python-net/aspose.words.drawing/shapebase/coord_size/
---

## ShapeBase.coord_size property

The width and height of the coordinate space inside the containing block of this shape.


```python
@property
def coord_size(self) -> aspose.pydrawing.Size:
    ...

@coord_size.setter
def coord_size(self, value: aspose.pydrawing.Size):
    ...

```

### Remarks

The default value is (1000, 1000).




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

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```python
doc = aw.Document()
# Bir grup şekil ekleyin ve onu aşağıdan 100 puan ve sağdan 100 puan konumlandırın
# belgenin x ve Y koordinat başlangıç noktasını.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# "LocalToParent" yöntemini kullanarak grup içindeki x ve y koordinatlarında (0, 0) noktasını belirleyin
# (100, 100) koordinatı, üst şeklin koordinat sisteminde yer alır. Grup şeklinin ebeveyni doğrudan belgedir.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# Varsayılan olarak, bir şeklin iç koordinat düzlemi sol üst köşesi (0, 0) noktasındadır,
# ve sağ alt köşesi (1000, 1000) noktasındadır. Boyutu nedeniyle grup şeklimiz 500pt x 500pt bir alanı kaplar
# belgenin düzleminde. Bu, belgenin koordinat düzleminde 1pt hareketin
# grup şeklinin koordinat düzleminde 2pt hareket anlamına geldiği anlamına gelir.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Grup şeklinin x ve y eksen başlangıç noktasını sol üst köşeden merkeze taşıyın.
# Bu, grup iç koordinatlarını belgenin koordinatlarına göre daha da kaydıracak.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Koordinat düzleminin ölçeğini değiştirmek aynı zamanda göreli konumları da etkiler.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Bu gruba bir şekil eklemek ve konumunu belgedeki bir konuma göre tanımlamak istiyorsak,
# önce grup şekli içinde belgenin konumuyla eşleşecek bir konumu doğrulamamız gerekir.
self.assertEqual(aspose.pydrawing.PointF(700, 700), group.local_to_parent(aspose.pydrawing.PointF(350, 350)))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
group.append_child(shape)
doc.first_section.body.first_paragraph.append_child(group)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.LocalToParent.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

