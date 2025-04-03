---
title: StructuredDocumentTagRangeStart.wordOpenXMLMinimal property
linktitle: wordOpenXMLMinimal property
articleTitle: wordOpenXMLMinimal property
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTagRangeStart.wordOpenXMLMinimal property. Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../../aspose.words/saveformat/#FlatOpc) format."
type: docs
weight: 180
url: /nodejs-net/aspose.words.markup/structureddocumenttagrangestart/wordOpenXMLMinimal/
---

## StructuredDocumentTagRangeStart.wordOpenXMLMinimal property

Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../../aspose.words/saveformat/#FlatOpc) format.

Unlike the [StructuredDocumentTagRangeStart.wordOpenXML](../wordOpenXML/) property, this method generates a stripped-down document that excludes any non-content-related parts.



```js
get wordOpenXMLMinimal(): string
```

### Examples

Shows how to get minimal XML contained within the node in the FlatOpc format.

```js
let doc = new aw.Document(base.myDir + "Multi-section structured document tags.docx");
let tag = doc.getChild(aw.NodeType.StructuredDocumentTagRangeStart, 0, true).asStructuredDocumentTagRangeStart();

expect(tag.wordOpenXMLMinimal.includes("<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">"))
  .toEqual(true);
expect(tag.wordOpenXMLMinimal.includes("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\"")).toEqual(false);
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTagRangeStart](../)

