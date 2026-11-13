---
title: DocumentBuilder.current_story property
linktitle: current_story property
articleTitle: current_story property
second_title: Aspose.Words for Python
description: "DocumentBuilder.current_story property. Gets the story that is currently selected in this [DocumentBuilder](../)."
type: docs
weight: 70
url: /es/python-net/aspose.words/documentbuilder/current_story/
---

## DocumentBuilder.current_story property

Gets the story that is currently selected in this [DocumentBuilder](../).



```python
@property
def current_story(self) -> aspose.words.Story:
    ...

```

### Examples

Shows how to work with a document builder's current story.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Una Story es un tipo de nodo que tiene nodos Paragraph hijos, como un Body.
self.assertEqual(builder.current_story, doc.first_section.body)
self.assertEqual(builder.current_story, builder.current_paragraph.parent_node)
self.assertEqual(aw.StoryType.MAIN_TEXT, builder.current_story.story_type)
builder.current_story.append_paragraph('Text added to current Story.')
# Una Story también puede contener tablas.
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1')
builder.insert_cell()
builder.write('Row 1, cell 2')
builder.end_table()
self.assertTrue(builder.current_story.tables.contains(table))
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

