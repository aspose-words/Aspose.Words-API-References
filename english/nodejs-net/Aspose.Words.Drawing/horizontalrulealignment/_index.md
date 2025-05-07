---
title: HorizontalRuleAlignment enumeration
linktitle: HorizontalRuleAlignment enumeration
articleTitle: HorizontalRuleAlignment enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.HorizontalRuleAlignment enumeration. Represents the alignment for the specified horizontal rule."
type: docs
weight: 190
url: /nodejs-net/aspose.words.drawing/horizontalrulealignment/
---

## HorizontalRuleAlignment enumeration

Represents the alignment for the specified horizontal rule.


### Members

| Name | Description |
| --- | --- |
| Left | Aligned to the left. |
| Center | Aligned to the center. |
| Right | Aligned to the right. |

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

* module [Aspose.Words.Drawing](../)

