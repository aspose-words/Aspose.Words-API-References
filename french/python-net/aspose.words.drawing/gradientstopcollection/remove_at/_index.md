---
title: GradientStopCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "GradientStopCollection.remove_at method. Removes a [GradientStop](../../gradientstop/) from the collection at a specified index."
type: docs
weight: 60
url: /fr/python-net/aspose.words.drawing/gradientstopcollection/remove_at/
---

## remove_at(index) {#int}

Removes a [GradientStop](../../gradientstop/) from the collection at a specified index.



```python
def remove_at(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Returns

Removed [GradientStop](../../gradientstop/).


### Examples

Shows how to add gradient stops to the gradient fill.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
shape.fill.two_color_gradient(color1=aspose.pydrawing.Color.green, color2=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2)
# Obtenez la collection des arrêts de dégradé.
gradient_stops = shape.fill.gradient_stops
# Modifiez le premier arrêt de dégradé.
gradient_stops[0].color = aspose.pydrawing.Color.aqua
gradient_stops[0].position = 0.1
gradient_stops[0].transparency = 0.25
# Ajoutez un nouvel arrêt de dégradé à la fin de la collection.
gradient_stop = aw.drawing.GradientStop(color=aspose.pydrawing.Color.brown, position=0.5)
gradient_stops.add(gradient_stop)
# Supprimez l'arrêt de dégradé à l'index 1.
gradient_stops.remove_at(1)
# Et insérez un nouvel arrêt de dégradé au même index 1.
gradient_stops.insert(1, aw.drawing.GradientStop(color=aspose.pydrawing.Color.chocolate, position=0.75, transparency=0.3))
# Supprimez le dernier arrêt de dégradé dans la collection.
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
# Utilisez l'option de conformité pour définir la forme en utilisant DML
# si vous voulez obtenir la propriété "GradientStops" après l'enregistrement du document.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientStops.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [GradientStopCollection](../)

