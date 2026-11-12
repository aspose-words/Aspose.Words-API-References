---
title: ShapeBase.bounds_in_points property
linktitle: bounds_in_points property
articleTitle: bounds_in_points property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_in_points property. Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape."
type: docs
weight: 80
url: /tr/python-net/aspose.words.drawing/shapebase/bounds_in_points/
---

## ShapeBase.bounds_in_points property

Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.


```python
@property
def bounds_in_points(self) -> aspose.pydrawing.RectangleF:
    ...

```

### Remarks

The returned bounds do not include the rotation of this shape or the rotation of the parent group shape, if any.


### Examples

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

