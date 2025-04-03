---
title: OfficeMath.nodeType property
linktitle: nodeType property
articleTitle: nodeType property
second_title: Aspose.Words for NodeJs
description: "OfficeMath.nodeType property. Returns [NodeType.OfficeMath](../../../aspose.words/nodetype/#OfficeMath)."
type: docs
weight: 40
url: /nodejs-net/aspose.words.math/officemath/nodeType/
---

## OfficeMath.nodeType property

Returns [NodeType.OfficeMath](../../../aspose.words/nodetype/#OfficeMath).



```js
get nodeType(): Aspose.Words.NodeType
```

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

