---
title: OfficeMath.displayType property
linktitle: displayType property
articleTitle: displayType property
second_title: Aspose.Words for NodeJs
description: "OfficeMath.displayType property. Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text or displayed on its own line."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Math/officemath/displayType/
---

## OfficeMath.displayType property

Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text
or displayed on its own line.


```js
get displayType(): Aspose.Words.Math.OfficeMathDisplayType
```

### Remarks

Display format type has effect for top level Office Math only.

Returned display format type is always [OfficeMathDisplayType.Inline](../../officemathdisplaytype/#Inline) for nested Office Math.




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

* module [Aspose.Words.Math](../../)
* class [OfficeMath](../)

