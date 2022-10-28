---
title: GradientStopCollection class
second_title: Aspose.Words for Python via .NET API Reference
description: "Contains a collection of [GradientStop](../gradientstop/) objects"
type: docs
weight: 100
url: /python-net/aspose.words.drawing/gradientstopcollection/
---

## GradientStopCollection class

Contains a collection of [GradientStop](../gradientstop/) objects.
To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/net/working-with-graphic-elements/) documentation article.




You do not create instances of this class directly.
Use the [Fill.gradient_stops](../fill/gradient_stops/) property to access gradient stops of fill objects.



### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets a [GradientStop](../gradientstop/) object in the collection. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets an integer value indicating the number of items in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(gradient_stop)](./add/#gradientstop) | Adds a specified [GradientStop](../gradientstop/) to a gradient. |
|[ insert(index, gradient_stop)](./insert/#int_gradientstop) | Inserts a [GradientStop](../gradientstop/) to the collection at a specified index. |
|[ remove(gradient_stop)](./remove/#gradientstop) | Removes a specified [GradientStop](../gradientstop/) from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a [GradientStop](../gradientstop/) from the collection at a specified index. |

### Examples

Shows how to add gradient stops to the gradient fill.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, 80, 80)
shape.fill.two_color_gradient(drawing.Color.green, drawing.Color.red, aw.drawing.GradientStyle.HORIZONTAL, aw.drawing.GradientVariant.VARIANT2)

# Get gradient stops collection.
gradient_stops = shape.fill.gradient_stops

# Change first gradient stop.
gradient_stops[0].color = drawing.Color.aqua
gradient_stops[0].position = 0.1
gradient_stops[0].transparency = 0.25

# Add new gradient stop to the end of collection.
gradient_stop = aw.drawing.GradientStop(drawing.Color.brown, 0.5)
gradient_stops.add(gradient_stop)

# Remove gradient stop at index 1.
gradient_stops.remove_at(1)
# And insert new gradient stop at the same index 1.
gradient_stops.insert(1, aw.drawing.GradientStop(drawing.Color.chocolate, 0.75, 0.3))

# Remove last gradient stop in the collection.
gradient_stop = gradient_stops[2]
gradient_stops.remove(gradient_stop)

self.assertEqual(2, gradient_stops.count)

self.assertEqual(drawing.Color.aqua.to_argb(), gradient_stops[0].color.to_argb())
self.assertAlmostEqual(0.1, gradient_stops[0].position, delta=0.01)
self.assertAlmostEqual(0.25, gradient_stops[0].transparency, delta=0.01)

self.assertEqual(drawing.Color.chocolate.to_argb(), gradient_stops[1].color.to_argb())
self.assertAlmostEqual(0.75, gradient_stops[1].position, delta=0.01)
self.assertAlmostEqual(0.3, gradient_stops[1].transparency, delta=0.01)

# Use the compliance option to define the shape using DML
# if you want to get "gradient_stops" property after the document saves.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT

doc.save(ARTIFACTS_DIR + "Shape.gradient_stops.docx", save_options)
```

### See Also

* module [aspose.words.drawing](../)

