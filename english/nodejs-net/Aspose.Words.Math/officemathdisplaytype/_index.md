---
title: OfficeMathDisplayType enumeration
linktitle: OfficeMathDisplayType enumeration
articleTitle: OfficeMathDisplayType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Math.OfficeMathDisplayType enumeration. Specifies the display format type of the equation."
type: docs
weight: 30
url: /nodejs-net/aspose.words.math/officemathdisplaytype/
---

## OfficeMathDisplayType enumeration

Specifies the display format type of the equation.


### Members

| Name | Description |
| --- | --- |
| Display | The Office Math is displayed on its own line. |
| Inline | The Office Math is displayed inline with the text. |

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

