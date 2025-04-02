---
title: Story.lastParagraph property
linktitle: lastParagraph property
articleTitle: lastParagraph property
second_title: Aspose.Words for NodeJs
description: "Story.lastParagraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words/story/lastParagraph/
---

## Story.lastParagraph property

Gets the last paragraph in the story.


```js
get lastParagraph(): Aspose.Words.Paragraph
```

### Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Run 1. ");

// The document builder has a cursor, which acts as the part of the document
// where the builder appends new nodes when we use its document construction methods.
// This cursor functions in the same way as Microsoft Word's blinking cursor,
// and it also always ends up immediately after any node that the builder just inserted.
// To append content to a different part of the document,
// we can move the cursor to a different node with the "MoveTo" method.
expect(builder.currentParagraph).toEqual(doc.firstSection.body.lastParagraph);
builder.moveTo(doc.firstSection.body.firstParagraph.runs.at(0));
expect(builder.currentParagraph).toEqual(doc.firstSection.body.firstParagraph);

// The cursor is now in front of the node that we moved it to.
// Adding a second run will insert it in front of the first run.
builder.writeln("Run 2. ");

expect(doc.getText().trim()).toEqual("Run 2. \rRun 1.");

// Move the cursor to the end of the document to continue appending text to the end as before.
builder.moveTo(doc.lastSection.body.lastParagraph);
builder.writeln("Run 3. ");

expect(doc.getText().trim()).toEqual("Run 2. \rRun 1. \rRun 3.");
expect(builder.currentParagraph).toEqual(doc.firstSection.body.lastParagraph);
```

### See Also

* module [Aspose.Words](../../)
* class [Story](../)

