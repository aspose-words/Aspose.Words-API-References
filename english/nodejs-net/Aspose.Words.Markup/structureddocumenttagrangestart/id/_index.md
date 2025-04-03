---
title: StructuredDocumentTagRangeStart.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTagRangeStart.id property. Specifies a unique read-only persistent numerical Id for this structured document tag."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttagrangestart/id/
---

## StructuredDocumentTagRangeStart.id property

Specifies a unique read-only persistent numerical Id for this structured document tag.




```js
get id(): number
```

### Remarks

Id attribute shall follow these rules:

* The document shall retain structured document tag ids only if the whole document
  is cloned [Document.clone()](../../../aspose.words/document/clone/#default).
  
* During [DocumentBase.importNode()](../../../aspose.words/documentbase/importNode/#node_boolean)
  Id shall be retained if import does not cause conflicts with other structured document tag Ids in
  the target document.
  
* If multiple structured document tag nodes specify the same decimal number value for the Id attribute,
  then the first structured document tag in the document shall maintain this original Id,
  and all subsequent structured document tag nodes shall have new identifiers assigned to them when the document is loaded.
  
* During standalone structured document tag Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener) operation new unique ID will be
  generated for the cloned structured document tag node.
  
* If Id is not specified in the source document, then the structured document tag node shall have a new unique identifier assigned
  to it when the document is loaded.
  





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

