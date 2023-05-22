---
title: HeaderFooter.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "HeaderFooter.node_type property. Returns [NodeType.HEADER_FOOTER](../../nodetype/#HEADER_FOOTER)."
type: docs
weight: 50
url: /python-net/aspose.words/headerfooter/node_type/
---

## HeaderFooter.node_type property

Returns [NodeType.HEADER_FOOTER](../../nodetype/#HEADER_FOOTER).



### Examples

Shows how to iterate through the children of a composite node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Section 1")
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write("Primary header")
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write("Primary footer")

section = doc.first_section

# A Section is a composite node and can contain child nodes,
# but only if those child nodes are of a "BODY" or "HEADER_FOOTER" node type.
for node in section:
    if node.node_type == aw.NodeType.BODY:
        body = node.as_body()
        print("Body:")
        print(f"\t\"{body.get_text().strip()}\"")
    elif node.node_type == aw.NodeType.HEADER_FOOTER:
        header_footer = node.as_header_footer()
        print(f"HeaderFooter type: {header_footer.header_footer_type}:")
        print(f"\t\"{header_footer.get_text().strip()}\"")
    else:
        raise Exception("Unexpected node type in a section.")
```

### See Also

* module [aspose.words](../../)
* class [HeaderFooter](../)

