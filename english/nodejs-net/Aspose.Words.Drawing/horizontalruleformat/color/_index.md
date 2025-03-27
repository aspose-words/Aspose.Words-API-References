---
title: HorizontalRuleFormat.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for NodeJs
description: "HorizontalRuleFormat.color property. Gets or sets the brush color that fills the horizontal rule."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Drawing/horizontalruleformat/color/
---

## HorizontalRuleFormat.color property

Gets or sets the brush color that fills the horizontal rule.


```js
get color(): string
```

### Remarks

This is a shortcut to the [Fill.color](../../fill/color/) property.

The default value is
aspose.pydrawing.Color.gray.





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

