---
title: DocumentBuilder.currentStory property
linktitle: currentStory property
articleTitle: currentStory property
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.currentStory property. Gets the story that is currently selected in this [DocumentBuilder](../)."
type: docs
weight: 70
url: /nodejs-net/aspose.words/documentbuilder/currentStory/
---

## DocumentBuilder.currentStory property

Gets the story that is currently selected in this [DocumentBuilder](../).



```js
get currentStory(): Aspose.Words.Story
```

### Examples

Shows how to work with a document builder's current story.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// A Story is a type of node that has child Paragraph nodes, such as a Body.
expect(doc.firstSection.body.referenceEquals(builder.currentStory)).toBe(true);
expect(builder.currentParagraph.parentNode.referenceEquals(builder.currentStory)).toBe(true);
expect(builder.currentStory.storyType == aw.StoryType.MainText).toBe(true);

builder.currentStory.appendParagraph("Text added to current Story.");

// A Story can also contain tables.
let table = builder.startTable();
builder.insertCell();
builder.write("Row 1, cell 1");
builder.insertCell();
builder.write("Row 1, cell 2");
builder.endTable();

expect(builder.currentStory.tables.contains(table)).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

