---
title: StructuredDocumentTagRangeStart.tag property
linktitle: tag property
articleTitle: tag property
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTagRangeStart.tag property. Specifies a tag associated with the current structured document tag node"
type: docs
weight: 150
url: /nodejs-net/aspose.words.markup/structureddocumenttagrangestart/tag/
---

## StructuredDocumentTagRangeStart.tag property

Specifies a tag associated with the current structured document tag node.
Can not be ``null``.



```js
get tag(): string
```

### Remarks

A tag is an arbitrary string which applications can associate with structured document
tag in order to identify it without providing a visible friendly name.


### Examples

Shows how to get the properties of multi-section structured document tags.

```js
let doc = new aw.Document(base.myDir + "Multi-section structured document tags.docx");

let rangeStartTag = doc.getChildNodes(aw.NodeType.StructuredDocumentTagRangeStart, true).at(0).asStructuredDocumentTagRangeStart();
let rangeEndTag = doc.getChildNodes(aw.NodeType.StructuredDocumentTagRangeEnd, true).at(0).asStructuredDocumentTagRangeEnd();

expect(rangeEndTag.id).toEqual(rangeStartTag.id);
expect(rangeStartTag.nodeType).toEqual(aw.NodeType.StructuredDocumentTagRangeStart);
expect(rangeEndTag.nodeType).toEqual(aw.NodeType.StructuredDocumentTagRangeEnd);

console.log("StructuredDocumentTagRangeStart values:");
console.log(`\t|Id: ${rangeStartTag.id}`);
console.log(`\t|Title: ${rangeStartTag.title}`);
console.log(`\t|PlaceholderName: ${rangeStartTag.placeholderName}`);
console.log(`\t|IsShowingPlaceholderText: ${rangeStartTag.isShowingPlaceholderText}`);
console.log(`\t|LockContentControl: ${rangeStartTag.lockContentControl}`);
console.log(`\t|LockContents: ${rangeStartTag.lockContents}`);
console.log(`\t|Level: ${rangeStartTag.level}`);
console.log(`\t|NodeType: ${rangeStartTag.nodeType}`);
console.log(`\t|RangeEnd.NodeType: ${rangeStartTag.rangeEnd.nodeType}`);
console.log(`\t|Color: ${rangeStartTag.color}`);
console.log(`\t|SdtType: ${rangeStartTag.sdtType}`);
console.log(`\t|FlatOpcContent: ${rangeStartTag.wordOpenXML}`);
console.log(`\t|Tag: ${rangeStartTag.tag}\n`);

console.log("StructuredDocumentTagRangeEnd values:");
console.log(`\t|Id: ${rangeEndTag.id}`);
console.log(`\t|NodeType: ${rangeEndTag.nodeType}`);
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTagRangeStart](../)

