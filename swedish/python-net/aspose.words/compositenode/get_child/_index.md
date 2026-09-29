---
title: CompositeNode.get_child method
linktitle: get_child method
articleTitle: get_child method
second_title: Aspose.Words for Python
description: "CompositeNode.get_child method. Returns an Nth child node that matches the specified type."
type: docs
weight: 90
url: /sv/python-net/aspose.words/compositenode/get_child/
---

## get_child(node_type, index, is_deep) {#nodetype_int_bool}

Returns an Nth child node that matches the specified type.


```python
def get_child(self, node_type: aspose.words.NodeType, index: int, is_deep: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node_type | [NodeType](../../nodetype/) | Specifies the type of the child node. |
| index | int | Zero based index of the child node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| is_deep | bool | ``True`` to select from all child nodes recursively; ``False`` to select only among immediate children. See remarks for more info. |

### Remarks

If index is out of range, a ``None`` is returned.




Note that markup nodes ([NodeType.STRUCTURED_DOCUMENT_TAG](../../nodetype/#STRUCTURED_DOCUMENT_TAG) and [NodeType.SMART_TAG](../../nodetype/#SMART_TAG))
are traversed even when *isDeep* =``False`` and [CompositeNode.get_child()](./#nodetype_int_bool) is invoked for non-markup node type. For example if the first run in a para
is wrapped in a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), it will still be returned by [CompositeNode.get_child()](./#nodetype_int_bool)([NodeType.RUN](../../nodetype/#RUN), 0, ``False``).


### Returns

The child node that matches the criteria or ``None`` if no matching node is found.


### Examples

Shows how to apply the properties of a table's style directly to the table's elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Hello world!')
builder.end_table()
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
table_style.row_stripe = 3
table_style.cell_spacing = 5
table_style.shading.background_pattern_color = aspose.pydrawing.Color.antique_white
table_style.borders.color = aspose.pydrawing.Color.blue
table_style.borders.line_style = aw.LineStyle.DOT_DASH
table.style = table_style
# Denna metod gäller tabellstilegenskaper såsom de vi satte ovan.
doc.expand_table_styles_to_direct_formatting()
doc.save(file_name=ARTIFACTS_DIR + 'Document.TableStyleToDirectFormatting.docx')
```

Shows how to traverse through a composite node's collection of child nodes.

```python
doc = aw.Document()
# Lägg till två körningar och en form som barnnoder till det första stycket i detta dokument.
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
paragraph.append_child(aw.Run(doc=doc, text='Hello world! '))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
# Observera att 'CustomNodeId' inte sparas till en utdatafil och endast existerar under nodens livstid.
shape.custom_node_id = 100
shape.wrap_type = aw.drawing.WrapType.INLINE
paragraph.append_child(shape)
paragraph.append_child(aw.Run(doc=doc, text='Hello again!'))
# Iterera genom styckets samling av omedelbara underordnade,
# och skriv ut alla körningar eller former som vi hittar inom.
children = paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, False).count)
for child in children:
    switch_condition = child.node_type
    if switch_condition == aw.NodeType.RUN:
        print('Run contents:')
        print(f'\t"{child.get_text().strip()}"')
    elif switch_condition == aw.NodeType.SHAPE:
        child_shape = child.as_shape()
        print('Shape:')
        print(f'\t{child_shape.shape_type}, {child_shape.width}x{child_shape.height}')
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

