---
title: LoadOptions.convertShapeToOfficeMath property
linktitle: convertShapeToOfficeMath property
articleTitle: convertShapeToOfficeMath property
second_title: Aspose.Words for Node.js
description: "LoadOptions.convertShapeToOfficeMath property. Gets or sets whether to convert shapes with EquationXML to Office Math objects."
type: docs
weight: 40
url: /nodejs-net/aspose.words.loading/loadoptions/convertShapeToOfficeMath/
---

## LoadOptions.convertShapeToOfficeMath property

Gets or sets whether to convert shapes with EquationXML to Office Math objects.


```js
get convertShapeToOfficeMath(): boolean
```

### Examples

Shows how to convert EquationXML shapes to Office Math objects.

```js
let loadOptions = new aw.Loading.LoadOptions();

// Use this flag to specify whether to convert the shapes with EquationXML attributes
// to Office Math objects and then load the document.
loadOptions.convertShapeToOfficeMath = isConvertShapeToOfficeMath;

let doc = new aw.Document(base.myDir + "Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
  expect(doc.getChildNodes(aw.NodeType.Shape, true).count).toEqual(16);
  expect(doc.getChildNodes(aw.NodeType.OfficeMath, true).count).toEqual(34);
}
else
{
  expect(doc.getChildNodes(aw.NodeType.Shape, true).count).toEqual(24);
  expect(doc.getChildNodes(aw.NodeType.OfficeMath, true).count).toEqual(0);
}
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

