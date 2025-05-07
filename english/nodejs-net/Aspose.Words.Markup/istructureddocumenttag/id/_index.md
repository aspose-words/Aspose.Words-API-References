---
title: IStructuredDocumentTag.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for Node.js
description: "IStructuredDocumentTag.id property. Specifies a unique read-only persistent numerical Id for this SDT."
type: docs
weight: 30
url: /nodejs-net/aspose.words.markup/istructureddocumenttag/id/
---

## IStructuredDocumentTag.id property

Specifies a unique read-only persistent numerical Id for this **SDT**.




```js
get id(): number
```

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
* class [IStructuredDocumentTag](../)

