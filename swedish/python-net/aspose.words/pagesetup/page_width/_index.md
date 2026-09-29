---
title: PageSetup.page_width property
linktitle: page_width property
articleTitle: page_width property
second_title: Aspose.Words for Python
description: "PageSetup.page_width property. Returns or sets the width of the page in points."
type: docs
weight: 340
url: /sv/python-net/aspose.words/pagesetup/page_width/
---

## PageSetup.page_width property

Returns or sets the width of the page in points.


```python
@property
def page_width(self) -> float:
    ...

@page_width.setter
def page_width(self, value: float):
    ...

```

### Examples

Shows how to insert an image, and use it as a watermark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Infoga bilden i sidhuvudet så att den blir synlig på varje sida.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
# Placera bilden i mitten av sidan.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.left = (builder.page_setup.page_width - shape.width) / 2
shape.top = (builder.page_setup.page_height - shape.height) / 2
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertWatermark.docx')
```

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
* class [PageSetup](../)

