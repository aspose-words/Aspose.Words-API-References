﻿---
title: OfficeMath.parentParagraph property
linktitle: parentParagraph property
articleTitle: parentParagraph property
second_title: Aspose.Words for Node.js
description: "OfficeMath.parentParagraph property. Retrieves the parent [Paragraph](../../../aspose.words/paragraph/) of this node."
type: docs
weight: 50
url: /nodejs-net/aspose.words.math/officemath/parentParagraph/
---

## OfficeMath.parentParagraph property

Retrieves the parent [Paragraph](../../../aspose.words/paragraph/) of this node.



```js
get parentParagraph(): Aspose.Words.Paragraph
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

