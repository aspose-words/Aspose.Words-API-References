---
title: StructuredDocumentTagRangeStart.removeAllChildren method
linktitle: removeAllChildren method
articleTitle: removeAllChildren method
second_title: Aspose.Words for Node.js
description: "StructuredDocumentTagRangeStart.removeAllChildren method. Removes all the nodes between this range start node and the range end node."
type: docs
weight: 230
url: /nodejs-net/aspose.words.markup/structureddocumenttagrangestart/removeAllChildren/
---

## removeAllChildren() {#default}

Removes all the nodes between this range start node and the range end node.


```js
removeAllChildren()
```

### Examples

Shows how to create/remove structured document tag and its content.

```js
test('SdtRangeExtendedMethods', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);

  builder.writeln("StructuredDocumentTag element");

  let rangeStart = insertStructuredDocumentTagRanges(doc);

  // Removes ranged structured document tag, but keeps content inside.
  rangeStart.removeSelfOnly();

  rangeStart = doc.getChild(aw.NodeType.StructuredDocumentTagRangeStart, 0, false);
  expect(rangeStart).toEqual(null);

  let rangeEnd = doc.getChild(aw.NodeType.StructuredDocumentTagRangeEnd, 0, false);
  expect(rangeEnd).toEqual(null);
  expect(doc.getText().trim()).toEqual("StructuredDocumentTag element");

  rangeStart = insertStructuredDocumentTagRanges(doc);

  let paragraphNode = lastOrDefault(rangeStart);
  expect(paragraphNode).not.toBeNull();
  expect(paragraphNode.getText().trim()).toEqual("StructuredDocumentTag element");

  // Removes ranged structured document tag and content inside.
  rangeStart.removeAllChildren();

  paragraphNode = lastOrDefault(rangeStart);
  expect(paragraphNode).toBeNull();
});

function lastOrDefault(enumeratedObject) {
  let children = Array.from(enumeratedObject);
  return children.length == 0 ? null : children.at(-1);
}

function insertStructuredDocumentTagRanges(doc) {
  let rangeStart = new aw.Markup.StructuredDocumentTagRangeStart(doc, aw.Markup.SdtType.PlainText);
  let rangeEnd = new aw.Markup.StructuredDocumentTagRangeEnd(doc, rangeStart.id);

  doc.firstSection.body.insertBefore(rangeStart, doc.firstSection.body.firstParagraph);
  doc.lastSection.body.insertAfter(rangeEnd, doc.firstSection.body.firstParagraph);

  return rangeStart;
}
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTagRangeStart](../)

