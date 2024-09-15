---
title: Story.story_type property
linktitle: story_type property
articleTitle: story_type property
second_title: Aspose.Words for Python
description: "Story.story_type property. Gets the type of this story."
type: docs
weight: 40
url: /python-net/aspose.words/story/story_type/
---

## Story.story_type property

Gets the type of this story.


```python
@property
def story_type(self) -> aspose.words.StoryType:
    ...

```

### Examples

Shows how to remove all shapes from a node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Use a DocumentBuilder to insert a shape. This is an inline shape,
# which has a parent Paragraph, which is a child node of the first section's Body.
builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=100, height=100)
self.assertEqual(1, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
# We can delete all shapes from the child paragraphs of this Body.
self.assertEqual(aw.StoryType.MAIN_TEXT, doc.first_section.body.story_type)
doc.first_section.body.delete_shapes()
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

