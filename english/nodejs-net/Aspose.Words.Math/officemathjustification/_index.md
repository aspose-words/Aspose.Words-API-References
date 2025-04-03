---
title: OfficeMathJustification enumeration
linktitle: OfficeMathJustification enumeration
articleTitle: OfficeMathJustification enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Math.OfficeMathJustification enumeration. Specifies the justification of the equation."
type: docs
weight: 40
url: /nodejs-net/aspose.words.math/officemathjustification/
---

## OfficeMathJustification enumeration

Specifies the justification of the equation.


### Members

| Name | Description |
| --- | --- |
| CenterGroup | Justifies instances of mathematical text to the left with respect to each other, and centers the group of mathematical text (the Math Paragraph) with respect to the page. |
| Center | Centers each instance of mathematical text individually with respect to margins. |
| Left | Left justification of Math Paragraph. |
| Right | Right Justification of Math Paragraph. |
| Inline | Inline position of Math. |
| Default | Default value [OfficeMathJustification.CenterGroup](./#CenterGroup). |

### Examples

Shows how to set office math display formatting.

```js
let doc = new aw.Document(base.myDir + "Office math.docx");

let officeMath = doc.getOfficeMath(0, true);

// OfficeMath nodes that are children of other OfficeMath nodes are always inline.
// The node we are working with is the base node to change its location and display type.
expect(officeMath.mathObjectType).toEqual(aw.Math.MathObjectType.OMathPara);
expect(officeMath.nodeType).toEqual(aw.NodeType.OfficeMath);
expect(officeMath.parentParagraph.referenceEquals(officeMath.parentNode)).toBeTruthy();

// Change the location and display type of the OfficeMath node.
officeMath.displayType = aw.Math.OfficeMathDisplayType.Display;
officeMath.justification = aw.Math.OfficeMathJustification.Left;

doc.save(base.artifactsDir + "Shape.officeMath.docx");
```

### See Also

* module [Aspose.Words.Math](../)

