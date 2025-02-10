---
title: ListLabel.label_string property
linktitle: label_string property
articleTitle: label_string property
second_title: Aspose.Words for Python
description: "ListLabel.label_string property. Gets a string representation of list label."
type: docs
weight: 20
url: /python-net/aspose.words.lists/listlabel/label_string/
---

## ListLabel.label_string property

Gets a string representation of list label.


```python
@property
def label_string(self) -> str:
    ...

```

### Examples

Shows how to extract the list labels of all paragraphs that are list items.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
doc.update_list_labels()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
# Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
# which start at three and ends at six.
for paragraph in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'List item paragraph #{paras.index_of(paragraph)}')
    # This is the text we get when getting when we output this node to text format.
    # This text output will omit list labels. Trim any paragraph formatting characters.
    paragraph_text = paragraph.to_string(save_format=aw.SaveFormat.TEXT).strip()
    print(f'\tExported Text: {paragraph_text}')
    label = paragraph.list_label
    # This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
    # this will tell us what position it is on that level.
    print(f'\tNumerical Id: {label.label_value}')
    # Combine them together to include the list label with the text in the output.
    print(f'\tList label combined with text: {label.label_string} {paragraph_text}')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLabel](../)

