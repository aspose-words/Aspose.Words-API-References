---
title: Paragraph.list_format property
linktitle: list_format property
articleTitle: list_format property
second_title: Aspose.Words for Python
description: "Paragraph.list_format property. Provides access to the list formatting properties of the paragraph."
type: docs
weight: 150
url: /python-net/aspose.words/paragraph/list_format/
---

## Paragraph.list_format property

Provides access to the list formatting properties of the paragraph.


```python
@property
def list_format(self) -> aspose.words.lists.ListFormat:
    ...

```

### Examples

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
* class [Paragraph](../)

