---
title: HorizontalRuleFormat.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for NodeJs
description: "HorizontalRuleFormat.alignment property. Gets or sets the alignment of the horizontal rule."
type: docs
weight: 10
url: /nodejs-net/aspose.words.drawing/horizontalruleformat/alignment/
---

## HorizontalRuleFormat.alignment property

Gets or sets the alignment of the horizontal rule.


```js
get alignment(): Aspose.Words.Drawing.HorizontalRuleAlignment
```

### Remarks

The default value is [HorizontalRuleAlignment.Left](../../horizontalrulealignment/#Left).




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

