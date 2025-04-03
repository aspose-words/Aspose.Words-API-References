---
title: HorizontalRuleFormat.noShade property
linktitle: noShade property
articleTitle: noShade property
second_title: Aspose.Words for NodeJs
description: "HorizontalRuleFormat.noShade property. Indicates the presence of 3D shading for the horizontal rule"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Drawing/horizontalruleformat/noShade/
---

## HorizontalRuleFormat.noShade property

Indicates the presence of 3D shading for the horizontal rule.
If ``true``, then the horizontal rule is without 3D shading and solid color is used.



```js
get noShade(): boolean
```

### Remarks

The default value is ``false``.




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

