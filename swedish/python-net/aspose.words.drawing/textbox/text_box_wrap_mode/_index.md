---
title: TextBox.text_box_wrap_mode property
linktitle: text_box_wrap_mode property
articleTitle: text_box_wrap_mode property
second_title: Aspose.Words for Python
description: "TextBox.text_box_wrap_mode property. Determines how text wraps inside a shape."
type: docs
weight: 110
url: /sv/python-net/aspose.words.drawing/textbox/text_box_wrap_mode/
---

## TextBox.text_box_wrap_mode property

Determines how text wraps inside a shape.


```python
@property
def text_box_wrap_mode(self) -> aspose.words.drawing.TextBoxWrapMode:
    ...

@text_box_wrap_mode.setter
def text_box_wrap_mode(self, value: aspose.words.drawing.TextBoxWrapMode):
    ...

```

### Remarks

The default value is [TextBoxWrapMode.SQUARE](../../textboxwrapmode/#SQUARE).




### Examples

Shows how to set a wrapping mode for the contents of a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
text_box_shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=300, height=300)
text_box = text_box_shape.text_box
# Ställ in egenskapen "TextBoxWrapMode" till "TextBoxWrapMode.None" för att öka textrutans bredd
# för att rymma text, om den är tillräckligt stor.
# Ställ in egenskapen "TextBoxWrapMode" till "TextBoxWrapMode.Square" för att
# bryta all text i textrutan, samtidigt som dess dimensioner bevaras.
text_box.text_box_wrap_mode = text_box_wrap_mode
builder.move_to(text_box_shape.last_paragraph)
builder.font.size = 32
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextBoxContentsWrapMode.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

