---
title: Fill.patterned method
linktitle: patterned method
articleTitle: patterned method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Fill.patterned method"
type: docs
weight: 230
url: /nodejs-net/aspose.words.drawing/fill/patterned/
---

## patterned(patternType) {#patterntype}

Sets the specified fill to a pattern.


```js
patterned(patternType: Aspose.Words.Drawing.PatternType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| patternType | [PatternType](../../patterntype/) | [PatternType](../../patterntype/) |

## patterned(patternType, foreColor, backColor) {#patterntype_string_string}

Sets the specified fill to a pattern.


```js
patterned(patternType: Aspose.Words.Drawing.PatternType, foreColor: string, backColor: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| patternType | [PatternType](../../patterntype/) | [PatternType](../../patterntype/) |
| foreColor | string | The color of the foreground fill. |
| backColor | string | The color of the background fill. |

## Examples

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

## See Also

* module [Aspose.Words.Drawing](../../)
* class [Fill](../)

