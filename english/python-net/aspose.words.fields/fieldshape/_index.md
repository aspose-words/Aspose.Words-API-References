﻿---
title: FieldShape class
linktitle: FieldShape class
articleTitle: FieldShape class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldShape class. Implements the SHAPE field"
type: docs
weight: 950
url: /python-net/aspose.words.fields/fieldshape/
---

## FieldShape class

Implements the SHAPE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Retrieves the specified text.


**Inheritance:** [FieldShape](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldShape()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [text](./text/) | Gets or sets the text to retrieve. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

* module [aspose.words.fields](../)
* class [Field](../field/)

