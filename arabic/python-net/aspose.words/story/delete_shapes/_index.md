---
title: Story.delete_shapes method
linktitle: delete_shapes method
articleTitle: delete_shapes method
second_title: Aspose.Words for Python
description: "Story.delete_shapes method. Deletes all shapes from the text of this story."
type: docs
weight: 70
url: /ar/python-net/aspose.words/story/delete_shapes/
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
# استخدم DocumentBuilder لإدراج شكل. هذا شكل مضمن،
# الذي له فقرة أصلية، وهي عقدة فرعية لجسم القسم الأول.
builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=100, height=100)
self.assertEqual(1, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
# يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا الجسم.
self.assertEqual(aw.StoryType.MAIN_TEXT, doc.first_section.body.story_type)
doc.first_section.body.delete_shapes()
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

