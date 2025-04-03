---
title: Shape.horizontalRuleFormat property
linktitle: horizontalRuleFormat property
articleTitle: horizontalRuleFormat property
second_title: Aspose.Words for NodeJs
description: "Shape.horizontalRuleFormat property. Provides access to the properties of the horizontal rule shape"
type: docs
weight: 110
url: /nodejs-net/Aspose.Words.Drawing/shape/horizontalRuleFormat/
---

## Shape.horizontalRuleFormat property

Provides access to the properties of the horizontal rule shape.
For a shape that is not a horizontal rule, returns ``null``.



```js
get horizontalRuleFormat(): Aspose.Words.Drawing.HorizontalRuleFormat
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
* class [Shape](../)

