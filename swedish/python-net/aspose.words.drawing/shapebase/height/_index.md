---
title: ShapeBase.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for Python
description: "ShapeBase.height property. Gets or sets the height of the containing block of the shape."
type: docs
weight: 210
url: /sv/python-net/aspose.words.drawing/shapebase/height/
---

## ShapeBase.height property

Gets or sets the height of the containing block of the shape.


```python
@property
def height(self) -> float:
    ...

@height.setter
def height(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.




### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
# Konfigurera figurens \"RelativeHorizontalPosition\"-egenskap så att den behandlar värdet på \"Left\"-egenskapen
# som figurens horisontella avstånd, i punkter, från sidans vänstra sida.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
# Ställ in figurens horisontella avstånd från sidans vänstra sida till 100.
shape.left = 100
# Använd \"RelativeVerticalPosition\"-egenskapen på liknande sätt för att placera figuren 80pt under sidans överkant.
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80
# Ställ in figurens höjd, vilket automatiskt skalar bredden för att bevara dimensionerna.
shape.height = 125
self.assertEqual(125, shape.width)
# Egenskaperna \"Bottom\" och \"Right\" innehåller bildens nedre och högra kanter.
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPositionSize.docx')
```

Shows how to resize a shape with an image.

```python
# När vi infogar en bild med metoden "InsertImage" skalar byggaren formen som visar bilden så att
# när vi visar dokumentet med 100% zoom i Microsoft Word, visar formen bilden i dess faktiska storlek.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# En 400×400 bild kommer att skapa ett ImageData-objekt med en bildstorlek på 300×300pt.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Om en forms dimensioner matchar bilddataens dimensioner,
# så visar formen bilden i sin ursprungliga storlek.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Minska den totala storleken på formen med 50%.
# Skalningsfaktorer tillämpas på både bredd och höjd samtidigt för att bevara formens proportioner.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# När du ändrar storlek på formen förblir bilddataens storlek densamma.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Vi kan referera till bilddataens dimensioner för att tillämpa en skalning baserad på bildens storlek.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

