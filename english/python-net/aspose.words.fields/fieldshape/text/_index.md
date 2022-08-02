---
title: text property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the text to retrieve."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldshape/text/
---

## FieldShape.text property

Gets or sets the text to retrieve.


### Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
# but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
# The following field will display ".1", the RTL equivalent of list number "1.".
field = builder.insert_field(aw.fields.FieldType.FIELD_BIDI_OUTLINE, True).as_field_bidi_outline()
builder.writeln("שלום")

self.assertEqual(" BIDIOUTLINE ", field.get_field_code())

# Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
builder.insert_field(aw.fields.FieldType.FIELD_BIDI_OUTLINE, True)
builder.writeln("שלום")
builder.insert_field(aw.fields.FieldType.FIELD_BIDI_OUTLINE, True)
builder.writeln("שלום")

# Set the horizontal text alignment for every paragraph in the document to RTL.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True

# If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
# Otherwise, they will display "###".
doc.save(ARTIFACTS_DIR + "Field.field_bidi_outline.docx")
```

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# Open a document that was created in Microsoft Word 2003.
doc = aw.Document(MY_DIR + "Legacy fields.doc")

# If we open the Word document and press Alt+F9, we will see a SHAPE and an EMBED field.
# A SHAPE field is the anchor/canvas for an AutoShape object with the "In line with text" wrapping style enabled.
# An EMBED field has the same function, but for an embedded object,
# such as a spreadsheet from an external Excel document.
# However, these fields will not appear in the document's Fields collection.
self.assertEqual(0, doc.range.fields.count)

# These fields are supported only by old versions of Microsoft Word.
# The document loading process will convert these fields into Shape objects,
# which we can access in the document's node collection.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)

# The first Shape node corresponds to the SHAPE field in the input document,
# which is the inline canvas for the AutoShape.
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)

# The second Shape node is the AutoShape itself.
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)

# The third Shape is what was the EMBED field that contained the external spreadsheet.
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldShape](../)

