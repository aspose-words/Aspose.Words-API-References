﻿---
title: Fill.opacity property
linktitle: opacity property
articleTitle: opacity property
second_title: Aspose.Words for Node.js
description: "Fill.opacity property. Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque)."
type: docs
weight: 150
url: /nodejs-net/aspose.words.drawing/fill/opacity/
---

## Fill.opacity property

Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque).


```js
get opacity(): number
```

### Remarks

This property is the opposite of property [Fill.transparency](../transparency/).


### Examples

Shows how to fill a shape with a solid color.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Write some text, and then cover it with a floating shape.
builder.font.size = 32;
builder.writeln("Hello world!");

let shape = builder.insertShape(aw.Drawing.ShapeType.CloudCallout, aw.Drawing.RelativeHorizontalPosition.LeftMargin, 25,
  aw.Drawing.RelativeVerticalPosition.TopMargin, 25, 250, 150, aw.Drawing.WrapType.None);

// Use the "StrokeColor" property to set the color of the outline of the shape.
shape.strokeColor = "#5F9EA0";

// Use the "FillColor" property to set the color of the inside area of the shape.
shape.fillColor = "#ADD8E6";

// The "Opacity" property determines how transparent the color is on a 0-1 scale,
// with 1 being fully opaque, and 0 being invisible.
// The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
expect(shape.fill.opacity).toEqual(1.0);

// Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
shape.fill.opacity = 0.3;

doc.save(base.artifactsDir + "Shape.fill.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [Fill](../)

