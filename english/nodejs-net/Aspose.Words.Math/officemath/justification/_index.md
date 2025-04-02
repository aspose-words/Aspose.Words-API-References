---
title: OfficeMath.justification property
linktitle: justification property
articleTitle: justification property
second_title: Aspose.Words for NodeJs
description: "OfficeMath.justification property. Gets/sets Office Math justification."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Math/officemath/justification/
---

## OfficeMath.justification property

Gets/sets Office Math justification.


```js
get justification(): Aspose.Words.Math.OfficeMathJustification
```

### Remarks

Justification cannot be set to the Office Math with display format type [OfficeMathDisplayType.Inline](../../officemathdisplaytype/#Inline).

Inline justification cannot be set to the Office Math with display format type [OfficeMathDisplayType.Display](../../officemathdisplaytype/#Display).

Corresponding [OfficeMath.displayType](../displayType/) has to be set before setting Office Math justification.




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

