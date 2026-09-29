---
title: GradientStopCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "GradientStopCollection.add method. Adds a specified [GradientStop](../../gradientstop/) to a gradient."
type: docs
weight: 30
url: /sv/python-net/aspose.words.drawing/gradientstopcollection/add/
---

## add(gradient_stop) {#gradientstop}

Adds a specified [GradientStop](../../gradientstop/) to a gradient.



```python
def add(self, gradient_stop: aspose.words.drawing.GradientStop):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| gradient_stop | [GradientStop](../../gradientstop/) |  |

### Examples

Shows how to add gradient stops to the gradient fill.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
shape.fill.two_color_gradient(color1=aspose.pydrawing.Color.green, color2=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2)
# Hämta samlingen av gradientstopp.
gradient_stops = shape.fill.gradient_stops
# Ändra första gradientstoppet.
gradient_stops[0].color = aspose.pydrawing.Color.aqua
gradient_stops[0].position = 0.1
gradient_stops[0].transparency = 0.25
# Lägg till ett nytt gradientstopp i slutet av samlingen.
gradient_stop = aw.drawing.GradientStop(color=aspose.pydrawing.Color.brown, position=0.5)
gradient_stops.add(gradient_stop)
# Ta bort gradientstopp vid index 1.
gradient_stops.remove_at(1)
# Och infoga ett nytt gradientstopp på samma index 1.
gradient_stops.insert(1, aw.drawing.GradientStop(color=aspose.pydrawing.Color.chocolate, position=0.75, transparency=0.3))
# Ta bort den sista färggradientstoppen i samlingen.
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
# Använd efterlevnadsalternativet för att definiera formen med DML
# om du vill få egenskapen "GradientStops" efter att dokumentet sparats.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientStops.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [GradientStopCollection](../)

