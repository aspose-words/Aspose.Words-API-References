---
title: Section.delete_header_footer_shapes method
linktitle: delete_header_footer_shapes method
articleTitle: delete_header_footer_shapes method
second_title: Aspose.Words for Python
description: "Section.delete_header_footer_shapes method. Deletes all shapes (drawing objects) from the headers and footers of this section."
type: docs
weight: 120
url: /python-net/aspose.words/section/delete_header_footer_shapes/
---

## delete_header_footer_shapes() {#default}

Deletes all shapes (drawing objects) from the headers and footers of this section.


```python
def delete_header_footer_shapes(self):
    ...
```

### Examples

Shows how to remove all shapes from all headers footers in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Create a primary header with a shape.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=100)
# Create a primary footer with an image.
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.insert_image(file_name=IMAGE_DIR + 'Logo icon.ico')
self.assertEqual(1, doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_PRIMARY).get_child_nodes(aw.NodeType.SHAPE, True).count)
self.assertEqual(1, doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY).get_child_nodes(aw.NodeType.SHAPE, True).count)
# Remove all shapes from the headers and footers in the first section.
doc.first_section.delete_header_footer_shapes()
self.assertEqual(0, doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_PRIMARY).get_child_nodes(aw.NodeType.SHAPE, True).count)
self.assertEqual(0, doc.first_section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY).get_child_nodes(aw.NodeType.SHAPE, True).count)
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

