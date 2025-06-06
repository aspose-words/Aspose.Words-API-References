﻿---
title: HeaderFooter.nodeType property
linktitle: nodeType property
articleTitle: nodeType property
second_title: Aspose.Words for Node.js
description: "HeaderFooter.nodeType property. Returns [NodeType.HeaderFooter](../../nodetype/#HeaderFooter)."
type: docs
weight: 50
url: /nodejs-net/aspose.words/headerfooter/nodeType/
---

## HeaderFooter.nodeType property

Returns [NodeType.HeaderFooter](../../nodetype/#HeaderFooter).



```js
get nodeType(): Aspose.Words.NodeType
```

### Examples

Shows how to iterate through the children of a composite node.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Section 1");
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.write("Primary header");
builder.moveToHeaderFooter(aw.HeaderFooterType.FooterPrimary);
builder.write("Primary footer");

let section = doc.firstSection;

// A Section is a composite node and can contain child nodes,
// but only if those child nodes are of a "Body" or "HeaderFooter" node type.
for (let node of section)
{
  switch (node.nodeType)
  {
    case aw.NodeType.Body:
    {
      let body = node.asBody();

      console.log("Body:");
      console.log(`\t\"${body.getText().trim()}\"`);
      break;
    }
    case aw.NodeType.HeaderFooter:
    {
      let headerFooter = node.asHeaderFooter();

      console.log(`HeaderFooter type: ${headerFooter.headerFooterType}:`);
      console.log(`\t\"${headerFooter.getText().trim()}\"`);
      break;
    }
    default:
    {
      throw new Error("Unexpected node type in a section.");
    }
  }
}
```

### See Also

* module [Aspose.Words](../../)
* class [HeaderFooter](../)

