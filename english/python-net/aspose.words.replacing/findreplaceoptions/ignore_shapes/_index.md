---
title: FindReplaceOptions.ignore_shapes property
linktitle: ignore_shapes property
articleTitle: ignore_shapes property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_shapes property. Gets or sets a boolean value indicating either to ignore shapes within a text."
type: docs
weight: 110
url: /python-net/aspose.words.replacing/findreplaceoptions/ignore_shapes/
---

## FindReplaceOptions.ignore_shapes property

Gets or sets a boolean value indicating either to ignore shapes within a text.

The default value is ``False``.




```python
@property
def ignore_shapes(self) -> bool:
    ...

@ignore_shapes.setter
def ignore_shapes(self, value: bool):
    ...

```

### Examples

Shows how to ignore shapes while replacing text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit.')
builder.insert_shape(shape_type=aw.drawing.ShapeType.BALLOON, width=200, height=200)
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit.')
find_replace_options = aw.replacing.FindReplaceOptions()
find_replace_options.ignore_shapes = True
builder.document.range.replace(pattern='Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.', replacement='Lorem ipsum dolor sit amet, consectetur adipiscing elit.', options=find_replace_options)
self.assertEqual('Lorem ipsum dolor sit amet, consectetur adipiscing elit.', builder.document.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

