---
title: HorizontalRuleFormat.widthPercent property
linktitle: widthPercent property
articleTitle: widthPercent property
second_title: Aspose.Words for NodeJs
description: "HorizontalRuleFormat.widthPercent property. Gets or sets the length of the specified horizontal rule expressed as a percentage of the window width."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Drawing/horizontalruleformat/widthPercent/
---

## HorizontalRuleFormat.widthPercent property

Gets or sets the length of the specified horizontal rule expressed as a percentage of the window width.


```js
get widthPercent(): number
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

Valid values ​​range from 1 to 100 inclusive.

The default value is 100.




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

