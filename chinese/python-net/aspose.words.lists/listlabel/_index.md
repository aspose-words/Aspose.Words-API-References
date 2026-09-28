---
title: ListLabel class
linktitle: ListLabel class
articleTitle: ListLabel class
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListLabel class. Defines properties specific to a list label"
type: docs
weight: 40
url: /zh/python-net/aspose.words.lists/listlabel/
---

## ListLabel class

Defines properties specific to a list label.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/python-net/working-with-lists/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Gets the list label font. |
| [label_string](./label_string/) | Gets a string representation of list label. |
| [label_value](./label_value/) | Gets a numeric value for this label. |

### Examples

Shows how to extract the list labels of all paragraphs that are list items.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
doc.update_list_labels()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
# 查找是否存在段落列表。在我们的文档中，列表使用普通的阿拉伯数字，
# 它们从三开始，到六结束。
for paragraph in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'List item paragraph #{paras.index_of(paragraph)}')
    # 这是我们在将此节点输出为文本格式时得到的文本。
    # 此文本输出将省略列表标签。去除任何段落格式字符。
    paragraph_text = paragraph.to_string(save_format=aw.SaveFormat.TEXT).strip()
    print(f'\tExported Text: {paragraph_text}')
    label = paragraph.list_label
    # 这获取段落在列表当前层级中的位置。如果我们有一个多层级的列表，
    # 这将告诉我们它在该层级上的位置。
    print(f'\tNumerical Id: {label.label_value}')
    # 将它们组合在一起，以在输出中包含列表标签和文本。
    print(f'\tList label combined with text: {label.label_string} {paragraph_text}')
```

### See Also

* module [aspose.words.lists](../)

