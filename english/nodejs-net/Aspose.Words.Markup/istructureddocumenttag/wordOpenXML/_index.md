---
title: IStructuredDocumentTag.wordOpenXML property
linktitle: wordOpenXML property
articleTitle: wordOpenXML property
second_title: Aspose.Words for Node.js
description: "IStructuredDocumentTag.wordOpenXML property. Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../../aspose.words/saveformat/#FlatOpc) format."
type: docs
weight: 150
url: /nodejs-net/aspose.words.markup/istructureddocumenttag/wordOpenXML/
---

## IStructuredDocumentTag.wordOpenXML property

Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../../aspose.words/saveformat/#FlatOpc) format.



```js
get wordOpenXML(): string
```

### Examples

Shows how to get XML contained within the node in the FlatOpc format.

```js
let doc = new aw.Document(base.myDir + "Structured document tags.docx");

var tags = doc.getChildNodes(aw.NodeType.StructuredDocumentTag, true);

expect(tags.at(0).asStructuredDocumentTag().wordOpenXML.includes(
    "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">")).toEqual(true);
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [IStructuredDocumentTag](../)

