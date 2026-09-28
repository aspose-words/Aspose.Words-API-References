---
title: Paragraph.list_label property
linktitle: list_label property
articleTitle: list_label property
second_title: Aspose.Words for Python
description: "Paragraph.list_label property. Gets a [Paragraph.list_label](./) object that provides access to list numbering value and formatting for this paragraph."
type: docs
weight: 160
url: /zh/python-net/aspose.words/paragraph/list_label/
---

## Paragraph.list_label property

Gets a [Paragraph.list_label](./) object that provides access to list numbering value and formatting
for this paragraph.



```python
@property
def list_label(self) -> aspose.words.lists.ListLabel:
    ...

```

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

* module [aspose.words](../../)
* class [Paragraph](../)

