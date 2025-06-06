﻿---
title: Paragraph.getText method
linktitle: getText method
articleTitle: getText method
second_title: Aspose.Words for Node.js
description: "Paragraph.getText method. Gets the text of this paragraph including the end of paragraph character."
type: docs
weight: 250
url: /nodejs-net/aspose.words/paragraph/getText/
---

## getText() {#default}

Gets the text of this paragraph including the end of paragraph character.


```js
getText()
```

### Remarks

The text of all child nodes is concatenated and the end of paragraph character is appended as follows:


* If the paragraph is the last paragraph of [Body](../../body/), then
  Aspose.Words.ControlChar.SectionBreak (\\x000c) is appended.
  
* If the paragraph is the last paragraph of [Cell](../../../aspose.words.tables/cell/), then
  Aspose.Words.ControlChar.Cell (\\x0007) is appended.
  
* For all other paragraphs
  Aspose.Words.ControlChar.ParagraphBreak (\\r) is appended.
  
The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```js
let doc = new aw.Document();

// An empty document, by default, has one paragraph.
expect(doc.firstSection.body.paragraphs.count).toEqual(1);

// Composite nodes such as our paragraph can contain other composite and inline nodes as children.
let paragraph = doc.firstSection.body.firstParagraph;
let paragraphText = new aw.Run(doc, "Initial text. ");
paragraph.appendChild(paragraphText);

// Create three more run nodes.
let run1 = new aw.Run(doc, "Run 1. ");
let run2 = new aw.Run(doc, "Run 2. ");
let run3 = new aw.Run(doc, "Run 3. ");

// The document body will not display these runs until we insert them into a composite node
// that itself is a part of the document's node tree, as we did with the first run.
// We can determine where the text contents of nodes that we insert
// appears in the document by specifying an insertion location relative to another node in the paragraph.
expect(paragraph.getText().trim()).toEqual("Initial text.");

// Insert the second run into the paragraph in front of the initial run.
paragraph.insertBefore(run2, paragraphText);

expect(paragraph.getText().trim()).toEqual("Run 2. Initial text.");

// Insert the third run after the initial run.
paragraph.insertAfter(run3, paragraphText);

expect(paragraph.getText().trim()).toEqual("Run 2. Initial text. Run 3.");

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph.prependChild(run1);

expect(paragraph.getText().trim()).toEqual("Run 1. Run 2. Initial text. Run 3.");
expect(paragraph.getChildNodes(aw.NodeType.Any, true).count).toEqual(4);

// We can modify the contents of the run by editing and deleting existing child nodes.
//paragraph.getChildNodes(aw.NodeType.Run, true).toArray().at(1).text = "Updated run 2. ";
//paragraph.getChildNodes(aw.NodeType.Run, true).remove(paragraphText);
paragraph.getChildNodes(aw.NodeType.Run, true).toArray().at(1).asRun().text = "Updated run 2. ";
paragraph.getChildNodes(aw.NodeType.Run, true).remove(paragraphText);

expect(paragraph.getText().trim()).toEqual("Run 1. Updated run 2. Run 3.");
expect(paragraph.getChildNodes(aw.NodeType.Any, true).count).toEqual(3);
```

### See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

