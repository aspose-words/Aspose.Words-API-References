---
title: GradientStopCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "GradientStopCollection.count property. Gets an integer value indicating the number of items in the collection."
type: docs
weight: 20
url: /it/python-net/aspose.words.drawing/gradientstopcollection/count/
---

## GradientStopCollection.count property

Gets an integer value indicating the number of items in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to add gradient stops to the gradient fill.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
shape.fill.two_color_gradient(color1=aspose.pydrawing.Color.green, color2=aspose.pydrawing.Color.red, style=aw.drawing.GradientStyle.HORIZONTAL, variant=aw.drawing.GradientVariant.VARIANT2)
# Ottieni la raccolta dei gradient stop.
gradient_stops = shape.fill.gradient_stops
# Modifica il primo gradient stop.
gradient_stops[0].color = aspose.pydrawing.Color.aqua
gradient_stops[0].position = 0.1
gradient_stops[0].transparency = 0.25
# Aggiungi un nuovo gradient stop alla fine della raccolta.
gradient_stop = aw.drawing.GradientStop(color=aspose.pydrawing.Color.brown, position=0.5)
gradient_stops.add(gradient_stop)
# Rimuovi il gradient stop all'indice 1.
gradient_stops.remove_at(1)
# E inserisci un nuovo gradient stop allo stesso indice 1.
gradient_stops.insert(1, aw.drawing.GradientStop(color=aspose.pydrawing.Color.chocolate, position=0.75, transparency=0.3))
# Rimuovi l'ultimo punto di gradiente nella collezione.
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
# Usa l'opzione di conformità per definire la forma usando DML
# se vuoi ottenere la proprietà "GradientStops" dopo che il documento è stato salvato.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GradientStops.docx', save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [GradientStopCollection](../)

