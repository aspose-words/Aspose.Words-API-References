---
title: Story.delete_shapes method
linktitle: delete_shapes method
articleTitle: delete_shapes method
second_title: Aspose.Words for Python
description: "Story.delete_shapes method. Deletes all shapes from the text of this story."
type: docs
weight: 70
url: /sv/python-net/aspose.words/story/delete_shapes/
---

## delete_shapes() {#default}

Deletes all shapes from the text of this story.


```python
def delete_shapes(self):
    ...
```

### Examples

Shows how to remove all shapes from a node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Använd en DocumentBuilder för att infoga en form. Detta är en inline-form,
# som har ett föräldra-Paragraph, som är en barnnod till den första sektionens Body.
builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=100, height=100)
self.assertEqual(1, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
# Vi kan ta bort alla former från de underliggande styckena i detta Body.
self.assertEqual(aw.StoryType.MAIN_TEXT, doc.first_section.body.story_type)
doc.first_section.body.delete_shapes()
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

