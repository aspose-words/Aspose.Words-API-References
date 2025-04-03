---
title: HorizontalRuleFormat class
linktitle: HorizontalRuleFormat class
articleTitle: HorizontalRuleFormat class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.HorizontalRuleFormat class. Represents horizontal rule formatting"
type: docs
weight: 200
url: /nodejs-net/aspose.words.drawing/horizontalruleformat/
---

## HorizontalRuleFormat class

Represents horizontal rule formatting.
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/nodejs-net/working-with-shapes/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [alignment](./alignment/) | Gets or sets the alignment of the horizontal rule. |
| [color](./color/) | Gets or sets the brush color that fills the horizontal rule. |
| [height](./height/) | Gets or sets the height of the horizontal rule. |
| [noShade](./noShade/) | Indicates the presence of 3D shading for the horizontal rule. If ``true``, then the horizontal rule is without 3D shading and solid color is used. |
| [widthPercent](./widthPercent/) | Gets or sets the length of the specified horizontal rule expressed as a percentage of the window width. |

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

