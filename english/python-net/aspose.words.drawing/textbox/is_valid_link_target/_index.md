---
title: TextBox.is_valid_link_target method
linktitle: is_valid_link_target method
articleTitle: is_valid_link_target method
second_title: Aspose.Words for Python
description: "TextBox.is_valid_link_target method. Determines whether this [TextBox](../) can be linked to the target [TextBox](../)."
type: docs
weight: 140
url: /python-net/aspose.words.drawing/textbox/is_valid_link_target/
---

## is_valid_link_target(target) {#textbox}

Determines whether this [TextBox](../) can be linked to the target [TextBox](../).



```python
def is_valid_link_target(self, target: aspose.words.drawing.TextBox):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| target | [TextBox](../) |  |

### Examples

Shows how to link text boxes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

text_box_shape1 = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 100, 100)
text_box1 = text_box_shape1.text_box
builder.writeln()

text_box_shape2 = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 100, 100)
text_box2 = text_box_shape2.text_box
builder.writeln()

text_box_shape3 = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 100, 100)
text_box3 = text_box_shape3.text_box
builder.writeln()

text_box_shape4 = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 100, 100)
text_box4 = text_box_shape4.text_box

# Create links between some of the text boxes.
if text_box1.is_valid_link_target(text_box2):
    text_box1.next = text_box2

if text_box2.is_valid_link_target(text_box3):
    text_box2.next = text_box3

# Only an empty text box may have a link.
self.assertTrue(text_box3.is_valid_link_target(text_box4))

builder.move_to(text_box_shape4.last_paragraph)
builder.write("Hello world!")

self.assertFalse(text_box3.is_valid_link_target(text_box4))

if text_box1.next is not None and text_box1.previous is None:
    print("This TextBox is the head of the sequence")

if text_box2.next is not None and text_box2.previous is None:
    print("This TextBox is the middle of the sequence")

if text_box3.next is None and text_box3.previous is not None:
    print("This TextBox is the tail of the sequence")

    # Break the forward link between text_box2 and text_box3, and then verify that they are no longer linked.
    text_box3.previous.break_forward_link()

    self.assertIsNone(text_box2.next)
    self.assertIsNone(text_box3.previous)

doc.save(ARTIFACTS_DIR + "Shape.create_link_between_text_boxes.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

