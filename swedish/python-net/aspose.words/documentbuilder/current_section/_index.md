---
title: DocumentBuilder.current_section property
linktitle: current_section property
articleTitle: current_section property
second_title: Aspose.Words for Python
description: "DocumentBuilder.current_section property. Gets the section that is currently selected in this [DocumentBuilder](../)."
type: docs
weight: 60
url: /sv/python-net/aspose.words/documentbuilder/current_section/
---

## DocumentBuilder.current_section property

Gets the section that is currently selected in this [DocumentBuilder](../).



```python
@property
def current_section(self) -> aspose.words.Section:
    ...

```

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

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

