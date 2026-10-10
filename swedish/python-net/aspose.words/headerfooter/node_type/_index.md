---
title: HeaderFooter.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "HeaderFooter.node_type property. Returns [NodeType.HEADER_FOOTER](../../nodetype/#HEADER_FOOTER)."
type: docs
weight: 50
url: /sv/python-net/aspose.words/headerfooter/node_type/
---

## HeaderFooter.node_type property

Returns [NodeType.HEADER_FOOTER](../../nodetype/#HEADER_FOOTER).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to iterate through the children of a composite node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('Primary header')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('Primary footer')
section = doc.first_section
# En sektion är en sammansatt nod och kan innehålla undernoder,
# men endast om dessa undernoder är av typen "Body" eller "HeaderFooter".
for node in section:
    switch_condition = node.node_type
    if switch_condition == aw.NodeType.BODY:
        body = node.as_body()
        print('Body:')
        print(f'\t"{body.get_text().strip()}"')
    elif switch_condition == aw.NodeType.HEADER_FOOTER:
        header_footer = node.as_header_footer()
        print(f'HeaderFooter type: {header_footer.header_footer_type}:')
        print(f'\t"{header_footer.get_text().strip()}"')
    else:
        raise Exception('Unexpected node type in a section.')
```

### See Also

* module [aspose.words](../../)
* class [HeaderFooter](../)

