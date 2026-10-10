---
title: Fill.gradient_stops property
linktitle: gradient_stops property
articleTitle: gradient_stops property
second_title: Aspose.Words for Python
description: "Fill.gradient_stops property. Gets a collection of [GradientStop](../../gradientstop/) objects for the fill."
type: docs
weight: 110
url: /zh/python-net/aspose.words.drawing/fill/gradient_stops/
---

## Fill.gradient_stops property

Gets a collection of [GradientStop](../../gradientstop/) objects for the fill.



```python
@property
def gradient_stops(self) -> aspose.words.drawing.GradientStopCollection:
    ...

```

### Examples

Shows how to add gradient stops to the gradient fill.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
shape.fill.two_color_gradient(color1=aspose.pydrawing.Color.green, color2=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2)
# 获取渐变停止点集合。
gradient_stops = shape.fill.gradient_stops
# 更改第一个渐变停止点。
gradient_stops[0].color = aspose.pydrawing.Color.aqua
gradient_stops[0].position = 0.1
gradient_stops[0].transparency = 0.25
# 在集合末尾添加新的渐变停止点。
gradient_stop = aw.drawing.GradientStop(color=aspose.pydrawing.Color.brown, position=0.5)
gradient_stops.add(gradient_stop)
# 移除索引 1 处的渐变停止点。
gradient_stops.remove_at(1)
# 并在相同的索引 1 处插入新的渐变停止点。
gradient_stops.insert(1, aw.drawing.GradientStop(color=aspose.pydrawing.Color.chocolate, position=0.75, transparency=0.3))
# 删除集合中的最后一个渐变停止点。
gradient_stop = gradient_stops[2]
gradient_stops.remove(gradient_stop)
self.assertEqual(2, gradient_stops.count)
self.assertEqual(aspose.pydrawing.Color.from_argb(255, 0, 255, 255), gradient_stops[0].base_color)
self.assertEqual(aspose.pydrawing.Color.aqua.to_argb(), gradient_stops[0].color.to_argb())
self.assertAlmostEqual(0.1, gradient_stops[0].position, delta=0.01)
self.assertAlmostEqual(0.25, gradient_stops[0].transparency, delta=0.01)
self.assertEqual(aspose.pydrawing.Color.chocolate.to_argb(), gradient_stops[1].color.to_argb())
self.assertAlmostEqual(0.75, gradient_stops[1].position, delta=0.01)
self.assertAlmostEqual(0.3, gradient_stops[1].transparency, delta=0.01)
# 使用合规选项通过 DML 定义形状
# 如果您想在文档保存后获取 "GradientStops" 属性。
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientStops.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

