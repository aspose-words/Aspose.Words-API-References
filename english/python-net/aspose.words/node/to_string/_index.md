---
title: Node.to_string method
linktitle: to_string method
articleTitle: to_string method
second_title: Aspose.Words for Python
description: "aspose.words.Node.to_string method"
type: docs
weight: 500
url: /python-net/aspose.words/node/to_string/
---

## to_string(save_format) {#saveformat}

Exports the content of the node into a string in the specified format.


```python
def to_string(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../saveformat/) |  |

### Returns

The content of the node in the specified format.


## to_string(save_options) {#saveoptions}

Exports the content of the node into a string using the specified save options.


```python
def to_string(self, save_options: aspose.words.saving.SaveOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_options | [SaveOptions](../../../aspose.words.saving/saveoptions/) | Specifies the options that control how the node is saved. |

### Returns

The content of the node in the specified format.


## Examples

Shows how to extract the list labels of all paragraphs that are list items.

```python
doc = aw.Document(MY_DIR + 'Rendering.docx')
doc.update_list_labels()
paras = [node.as_paragraph() for node in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)]
# Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
# which start at three and ends at six.
for paragraph in paras:
    if paragraph.list_format.is_list_item:
        print(f'List item paragraph #{paras.index(paragraph)}')
        # This is the text we get when getting when we output this node to text format.
        # This text output will omit list labels. Strip any paragraph formatting characters.
        paragraph_text = paragraph.to_string(aw.SaveFormat.TEXT).strip()
        print(f'\tExported Text: {paragraph_text}')
        label = paragraph.list_label
        # This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
        # this will tell us what position it is on that level.
        print(f'\tNumerical Id: {label.label_value}')
        # Combine them together to include the list label with the text in the output.
        print(f'\tList label combined with text: {label.label_string} {paragraph_text}')
```

## See Also

* module [aspose.words](../../)
* class [Node](../)

