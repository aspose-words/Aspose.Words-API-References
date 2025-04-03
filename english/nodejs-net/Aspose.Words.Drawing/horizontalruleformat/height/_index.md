---
title: HorizontalRuleFormat.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for NodeJs
description: "HorizontalRuleFormat.height property. Gets or sets the height of the horizontal rule."
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing/horizontalruleformat/height/
---

## HorizontalRuleFormat.height property

Gets or sets the height of the horizontal rule.


```js
get height(): number
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

This is a shortcut to the [ShapeBase.height](../../shapebase/height/) property.

Valid values ​​range from 0 to 1584 inclusive.

The default value is 1.5.




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
* class [HorizontalRuleFormat](../)

