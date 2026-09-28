---
title: Story.story_type property
linktitle: story_type property
articleTitle: story_type property
second_title: Aspose.Words for Python
description: "Story.story_type property. Gets the type of this story."
type: docs
weight: 40
url: /de/python-net/aspose.words/story/story_type/
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
# Verwenden Sie einen DocumentBuilder, um eine Form einzufügen. Dies ist eine Inline-Form,
# die einen übergeordneten Paragraph hat, welcher ein Kindknoten des Body der ersten Sektion ist.
builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=100, height=100)
self.assertEqual(1, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
# Wir können alle Formen aus den Kindabsätzen dieses Body löschen.
self.assertEqual(aw.StoryType.MAIN_TEXT, doc.first_section.body.story_type)
doc.first_section.body.delete_shapes()
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

