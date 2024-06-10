---
title: CompositeNode.get_text method
linktitle: get_text method
articleTitle: get_text method
second_title: Aspose.Words for Python
description: "CompositeNode.get_text method. Gets the text of this node and of all its children."
type: docs
weight: 110
url: /python-net/aspose.words/compositenode/get_text/
---

## get_text() {#default}

Gets the text of this node and of all its children.


```python
def get_text(self):
    ...
```

### Remarks

The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows the difference between calling the GetText and ToString methods on a node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.insert_field(field_code='MERGEFIELD Field')
# GetText will retrieve the visible text as well as field codes and special characters.
self.assertEqual('\x13MERGEFIELD Field\x14«Field»\x15', doc.get_text().strip())
# ToString will give us the document's appearance if saved to a passed save format.
self.assertEqual('«Field»', doc.to_string(save_format=aw.SaveFormat.TEXT).strip())
```

Shows how to output all paragraphs in a document that are list items.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.list_format.apply_number_default()
builder.writeln('Numbered list item 1')
builder.writeln('Numbered list item 2')
builder.writeln('Numbered list item 3')
builder.list_format.remove_numbers()
builder.list_format.apply_bullet_default()
builder.writeln('Bulleted list item 1')
builder.writeln('Bulleted list item 2')
builder.writeln('Bulleted list item 3')
builder.list_format.remove_numbers()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
for para in paras:
    para = para.as_paragraph()
    if para.list_format.is_list_item:
        print(f'This paragraph belongs to list ID# {para.list_format.list.list_id}, number style "{para.list_format.list_level.number_style}"')
        print(f'\t"{para.get_text().strip()}"')
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

