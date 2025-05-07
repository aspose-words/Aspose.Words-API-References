---
title: Fill.pattern property
linktitle: pattern property
articleTitle: pattern property
second_title: Aspose.Words for Node.js
description: "Fill.pattern property. Gets a [PatternType](../../patterntype/) for the fill."
type: docs
weight: 160
url: /nodejs-net/aspose.words.drawing/fill/pattern/
---

## Fill.pattern property

Gets a [PatternType](../../patterntype/) for the fill.



```js
get pattern(): Aspose.Words.Drawing.PatternType
```

### Examples

Shows how to set pattern for a shape.

```js
let doc = new aw.Document(base.myDir + "Shape stroke pattern border.docx");

let shape = doc.getShape(0, true);
let fill = shape.fill;

console.log(`Pattern value is: ${fill.pattern}`);

// There are several ways specified fill to a pattern.
// 1 -  Apply pattern to the shape fill:
fill.patterned(aw.Drawing.PatternType.DiagonalBrick);

// 2 -  Apply pattern with foreground and background colors to the shape fill:
fill.patterned(aw.Drawing.PatternType.DiagonalBrick, "#00FFFF", "#FFE4C4");

doc.save(base.artifactsDir + "Shape.FillPattern.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [Fill](../)

