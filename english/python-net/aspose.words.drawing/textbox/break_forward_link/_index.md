---
title: TextBox.break_forward_link method
linktitle: break_forward_link method
articleTitle: break_forward_link method
second_title: Aspose.Words for Python
description: "TextBox.break_forward_link method. Breaks the link to the next [TextBox](../)."
type: docs
weight: 130
url: /python-net/aspose.words.drawing/textbox/break_forward_link/
---

## break_forward_link() {#default}

Breaks the link to the next [TextBox](../).



```python
def break_forward_link(self):
    ...
```

### Remarks

[TextBox.break_forward_link()](./#default) doesn't break all other links in the current sequence of shapes.
For example: 1-2-3-4 sequence and [TextBox.break_forward_link()](./#default) at the 2-nd textbox will create
two sequences 1-2, 3-4.



### Examples

Shows how to link text boxes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
text_box_shape1 = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=100, height=100)
text_box1 = text_box_shape1.text_box
builder.writeln()
text_box_shape2 = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=100, height=100)
text_box2 = text_box_shape2.text_box
builder.writeln()
text_box_shape3 = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=100, height=100)
text_box3 = text_box_shape3.text_box
builder.writeln()
text_box_shape4 = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=100, height=100)
text_box4 = text_box_shape4.text_box
# Create links between some of the text boxes.
if text_box1.is_valid_link_target(text_box2):
    text_box1.next = text_box2
if text_box2.is_valid_link_target(text_box3):
    text_box2.next = text_box3
# Only an empty text box may have a link.
self.assertTrue(text_box3.is_valid_link_target(text_box4))
builder.move_to(text_box_shape4.last_paragraph)
builder.write('Hello world!')
self.assertFalse(text_box3.is_valid_link_target(text_box4))
if text_box1.next != None and text_box1.previous == None:
    print('This TextBox is the head of the sequence')
if text_box2.next != None and text_box2.previous != None:
    print('This TextBox is the middle of the sequence')
if text_box3.next == None and text_box3.previous != None:
    print('This TextBox is the tail of the sequence')
    # Break the forward link between textBox2 and textBox3, and then verify that they are no longer linked.
    text_box3.previous.break_forward_link()
    self.assertTrue(text_box2.next == None)
    self.assertTrue(text_box3.previous == None)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.CreateLinkBetweenTextBoxes.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

