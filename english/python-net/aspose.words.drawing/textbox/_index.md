---
title: TextBox class
linktitle: TextBox class
articleTitle: TextBox class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.TextBox class. Defines attributes that specify how a text is displayed inside a shape"
type: docs
weight: 450
url: /python-net/aspose.words.drawing/textbox/
---

## TextBox class

Defines attributes that specify how a text is displayed inside a shape.
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article.




### Remarks

Use the [Shape.text_box](../shape/text_box/) property to access text properties of a shape.
You do not create instances of the [TextBox](./) class directly.




### Properties

| Name | Description |
| --- | --- |
| [fit_shape_to_text](./fit_shape_to_text/) | Determines whether Microsoft Word will grow the shape to fit text. |
| [internal_margin_bottom](./internal_margin_bottom/) | Specifies the inner bottom margin in points for a shape. |
| [internal_margin_left](./internal_margin_left/) | Specifies the inner left margin in points for a shape. |
| [internal_margin_right](./internal_margin_right/) | Specifies the inner right margin in points for a shape. |
| [internal_margin_top](./internal_margin_top/) | Specifies the inner top margin in points for a shape. |
| [layout_flow](./layout_flow/) | Determines the flow of the text layout in a shape. |
| [next](./next/) | Returns or sets a [TextBox](./) that represents the next [TextBox](./) in a sequence of shapes. |
| [no_text_rotation](./no_text_rotation/) | Gets or sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated. |
| [parent](./parent/) | Gets a parent shape for the [TextBox](./). |
| [previous](./previous/) | Returns a [TextBox](./) that represents the previous [TextBox](./) in a sequence of shapes. |
| [text_box_wrap_mode](./text_box_wrap_mode/) | Determines how text wraps inside a shape. |
| [vertical_anchor](./vertical_anchor/) | Specifies the vertical alignment of the text within a shape. |

### Methods

| Name | Description |
| --- | --- |
|[ break_forward_link()](./break_forward_link/#default) | Breaks the link to the next [TextBox](./). |
|[ is_valid_link_target(target)](./is_valid_link_target/#textbox) | Determines whether this [TextBox](./) can be linked to the target [TextBox](./). |

### Examples

Shows how to get a text box to resize itself to fit its contents tightly.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
text_box_shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=150, height=100)
text_box = text_box_shape.text_box
# Apply these values to both these members to get the parent shape to fit
# tightly around the text contents, ignoring the dimensions we have set.
text_box.fit_shape_to_text = True
text_box.text_box_wrap_mode = aw.drawing.TextBoxWrapMode.NONE
builder.move_to(text_box_shape.last_paragraph)
builder.write('Text fit tightly inside textbox.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextBoxFitShapeToText.docx')
```

Shows how to set internal margins for a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert another textbox with specific margins.
text_box_shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=100, height=100)
text_box = text_box_shape.text_box
text_box.internal_margin_top = 15
text_box.internal_margin_bottom = 15
text_box.internal_margin_left = 15
text_box.internal_margin_right = 15
builder.move_to(text_box_shape.last_paragraph)
builder.write('Text placed according to textbox margins.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextBoxMargins.docx')
```

Shows how to set the orientation of text inside a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
text_box_shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=150, height=100)
text_box = text_box_shape.text_box
# Move the document builder to inside the TextBox and add text.
builder.move_to(text_box_shape.last_paragraph)
builder.writeln('Hello world!')
builder.write('Hello again!')
# Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
text_box.layout_flow = layout_flow
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextBoxLayoutFlow.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [Shape.text_box](../shape/text_box/)

