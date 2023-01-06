---
title: NodeType enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the type of a Word document node."
type: docs
weight: 750
url: /python-net/aspose.words/nodetype/
---

## NodeType enumeration

Specifies the type of a Word document node.


### Members

| Name | Description |
| --- | --- |
| ANY | Indicates all node types. Allows to select all children. |
| DOCUMENT | A [Document](../document/) object that, as the root of the document tree, provides access to the entire Word document. |
| SECTION | A [Section](../section/) object that corresponds to one section in a Word document. |
| BODY | A [Body](../body/) object that contains the main text of a section (main text story). |
| HEADER_FOOTER | A [HeaderFooter](../headerfooter/) object that contains text of a particular header or footer inside a section. |
| TABLE | A [Table](../../aspose.words.tables/table/) object that represents a table in a Word document. |
| ROW | A row of a table. |
| CELL | A cell of a table row. |
| PARAGRAPH | A paragraph of text. |
| BOOKMARK_START | A beginning of a bookmark marker. |
| BOOKMARK_END | An end of a bookmark marker. |
| EDITABLE_RANGE_START | A beginning of an editable range. |
| EDITABLE_RANGE_END | An end of an editable range. |
| MOVE_FROM_RANGE_START | A beginning of an MoveFrom range. |
| MOVE_FROM_RANGE_END | An end of an MoveFrom range. |
| MOVE_TO_RANGE_START | A beginning of an MoveTo range. |
| MOVE_TO_RANGE_END | An end of an MoveTo range. |
| GROUP_SHAPE | A group of shapes, images, OLE objects or other group shapes. |
| SHAPE | A drawing object, such as an OfficeArt shape, image or an OLE object. |
| COMMENT | A comment in a Word document. |
| FOOTNOTE | A footnote or endnote in a Word document. |
| RUN | A run of text. |
| FIELD_START | A special character that designates the start of a Word field. |
| FIELD_SEPARATOR | A special character that separates the field code from the field result. |
| FIELD_END | A special character that designates the end of a Word field. |
| FORM_FIELD | A form field. |
| SPECIAL_CHAR | A special character that is not one of the more specific special character types. |
| SMART_TAG | A smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph |
| STRUCTURED_DOCUMENT_TAG | Allows to define customer-specific information and its means of presentation. |
| STRUCTURED_DOCUMENT_TAG_RANGE_START | A start of **ranged** structured document tag which accepts multi-sections content. |
| STRUCTURED_DOCUMENT_TAG_RANGE_END | A end of **ranged** structured document tag which accepts multi-sections content. |
| GLOSSARY_DOCUMENT | A glossary document within the main document. |
| BUILDING_BLOCK | A building block within a glossary document (e.g. glossary document entry). |
| COMMENT_RANGE_START | A marker node that represents the start of a commented range. |
| COMMENT_RANGE_END | A marker node that represents the end of a commented range. |
| OFFICE_MATH | An Office Math object. Can be equation, function, matrix or one of other mathematical objects. Can be a collection of mathematical object and also can contain some non-mathematical objects such as runs of text. |
| SUB_DOCUMENT | A subdocument node which is a link to another document. |
| SYSTEM | Reserved for internal use by Aspose.Words. |
| NULL | Reserved for internal use by Aspose.Words. |

### Examples

Shows how to traverse through a composite node's collection of child nodes.

```python
doc = aw.Document()

# Add two runs and one shape as child nodes to the first paragraph of this document.
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
paragraph.append_child(aw.Run(doc, "Hello world! "))

shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
# Note that the 'custom_node_id' is not saved to an output file and exists only during the node lifetime.
shape.custom_node_id = 100
shape.wrap_type = aw.drawing.WrapType.INLINE
paragraph.append_child(shape)

paragraph.append_child(aw.Run(doc, "Hello again!"))

# Iterate through the paragraph's collection of immediate children,
# and print any runs or shapes that we find within.
children = paragraph.child_nodes

self.assertEqual(3, paragraph.child_nodes.count)

for child in children:
    if child.node_type == aw.NodeType.RUN:
        print("Run contents:")
        print(f"\t\"{child.get_text().strip()}\"")

    elif child.node_type == aw.NodeType.SHAPE:
        child_shape = child.as_shape()
        print("Shape:")
        print(f"\t{child_shape.shape_type}, {child_shape.width}x{child_shape.height}")
```

### See Also

* module [aspose.words](../)

