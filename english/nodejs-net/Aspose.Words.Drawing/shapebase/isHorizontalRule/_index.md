---
title: ShapeBase.isHorizontalRule property
linktitle: isHorizontalRule property
articleTitle: isHorizontalRule property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.isHorizontalRule property. Returns ``true`` if this shape is a horizontal rule."
type: docs
weight: 240
url: /nodejs-net/aspose.words.drawing/shapebase/isHorizontalRule/
---

## ShapeBase.isHorizontalRule property

Returns ``true`` if this shape is a horizontal rule.



```js
get isHorizontalRule(): boolean
```

### Examples

Shows how to insert a horizontal rule shape, and customize its formatting.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let shape = builder.insertHorizontalRule();

let horizontalRuleFormat = shape.horizontalRuleFormat;
horizontalRuleFormat.alignment = aw.Drawing.HorizontalRuleAlignment.Center;
horizontalRuleFormat.widthPercent = 70;
horizontalRuleFormat.height = 3;
horizontalRuleFormat.color = "#0000FF";
horizontalRuleFormat.noShade = true;

expect(shape.isHorizontalRule).toEqual(true);
expect(shape.horizontalRuleFormat.noShade).toEqual(true);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

