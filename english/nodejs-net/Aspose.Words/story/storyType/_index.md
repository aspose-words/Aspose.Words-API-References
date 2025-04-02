---
title: Story.storyType property
linktitle: storyType property
articleTitle: storyType property
second_title: Aspose.Words for NodeJs
description: "Story.storyType property. Gets the type of this story."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/story/storyType/
---

## Story.storyType property

Gets the type of this story.


```js
get storyType(): Aspose.Words.StoryType
```

### Examples

Shows how to remove all shapes from a node.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Use a DocumentBuilder to insert a shape. This is an inline shape,
// which has a parent Paragraph, which is a child node of the first section's Body.
builder.insertShape(aw.Drawing.ShapeType.Cube, 100.0, 100.0);

expect(doc.getChildNodes(aw.NodeType.Shape, true).count).toEqual(1);

// We can delete all shapes from the child paragraphs of this Body.
expect(doc.firstSection.body.storyType).toEqual(aw.StoryType.MainText);
doc.firstSection.body.deleteShapes();

expect(doc.getChildNodes(aw.NodeType.Shape, true).count).toEqual(0);
```

### See Also

* module [Aspose.Words](../../)
* class [Story](../)

