---
title: Shape.fill_color property
linktitle: fill_color property
articleTitle: fill_color property
second_title: Aspose.Words for Python
description: "Shape.fill_color property. Defines the brush color that fills the closed path of the shape."
type: docs
weight: 50
url: /tr/python-net/aspose.words.drawing/shape/fill_color/
---

## Shape.fill_color property

Defines the brush color that fills the closed path of the shape.


```python
@property
def fill_color(self) -> aspose.pydrawing.Color:
    ...

@fill_color.setter
def fill_color(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

This is a shortcut to the [Fill.color](../../fill/color/) property.

The default value is
aspose.pydrawing.Color.white.





### Examples

Shows how to fill a shape with a solid color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Biraz metin yazın ve ardından onu yüzen bir şekille kapatın.
builder.font.size = 32
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CLOUD_CALLOUT, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=25, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=25, width=250, height=150, wrap_type=aw.drawing.WrapType.NONE)
# Şeklin dış hat rengini ayarlamak için \"StrokeColor\" özelliğini kullanın.
shape.stroke_color = aspose.pydrawing.Color.cadet_blue
# Şeklin iç bölge rengini ayarlamak için \"FillColor\" özelliğini kullanın.
shape.fill_color = aspose.pydrawing.Color.light_blue
# \"Opacity\" özelliği rengin ne kadar şeffaf olduğunu 0-1 ölçeğinde belirler,
# 1 tam opak, 0 ise görünmez demektir.
# Şeklin doldurması varsayılan olarak tam opaktır, bu yüzden bu şeklin üzerindeki metni göremeyiz.
self.assertEqual(1, shape.fill.opacity)
# Şeklin doldurma renginin opaklığını daha düşük bir değere ayarlayın, böylece altındaki metni görebiliriz.
shape.fill.opacity = 0.3
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Fill.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

