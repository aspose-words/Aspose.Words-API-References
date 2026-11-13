---
title: TextBox.is_valid_link_target method
linktitle: is_valid_link_target method
articleTitle: is_valid_link_target method
second_title: Aspose.Words for Python
description: "TextBox.is_valid_link_target method. Determines whether this [TextBox](../) can be linked to the target [TextBox](../)."
type: docs
weight: 140
url: /es/python-net/aspose.words.drawing/textbox/is_valid_link_target/
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
# Cree enlaces entre algunos de los cuadros de texto.
if text_box1.is_valid_link_target(text_box2):
    text_box1.next = text_box2
if text_box2.is_valid_link_target(text_box3):
    text_box2.next = text_box3
# Solo un cuadro de texto vacío puede tener un enlace.
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
    # Rompa el enlace directo entre textBox2 y textBox3, y luego verifique que ya no estén enlazados.
    text_box3.previous.break_forward_link()
    self.assertTrue(text_box2.next == None)
    self.assertTrue(text_box3.previous == None)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.CreateLinkBetweenTextBoxes.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

