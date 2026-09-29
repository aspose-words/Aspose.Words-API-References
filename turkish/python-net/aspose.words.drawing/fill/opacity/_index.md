---
title: Fill.opacity property
linktitle: opacity property
articleTitle: opacity property
second_title: Aspose.Words for Python
description: "Fill.opacity property. Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque)."
type: docs
weight: 150
url: /tr/python-net/aspose.words.drawing/fill/opacity/
---

## Fill.opacity property

Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque).


```python
@property
def opacity(self) -> float:
    ...

@opacity.setter
def opacity(self, value: float):
    ...

```

### Remarks

This property is the opposite of property [Fill.transparency](../transparency/).


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
* class [Fill](../)

