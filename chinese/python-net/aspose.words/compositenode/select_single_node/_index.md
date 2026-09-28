---
title: CompositeNode.select_single_node method
linktitle: select_single_node method
articleTitle: select_single_node method
second_title: Aspose.Words for Python
description: "CompositeNode.select_single_node method. Selects the first [Node](../../node/) that matches the XPath expression."
type: docs
weight: 200
url: /zh/python-net/aspose.words/compositenode/select_single_node/
---

## select_single_node(xpath) {#str}

Selects the first [Node](../../node/) that matches the XPath expression.



```python
def select_single_node(self, xpath: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xpath | str | The XPath expression. |

### Remarks

Only expressions with element names are supported at the moment. Expressions
that use attribute names are not supported.




### Returns

The first [Node](../../node/) that matches the XPath query or ``None`` if no matching node is found.


### Examples

Shows how to select certain nodes by using an XPath expression.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
# 此表达式将提取所有段落节点，
# 这些节点是文档中任何表格节点的后代。
node_list = doc.select_nodes('//Table//Paragraph')
# 使用枚举器遍历列表，并打印表格中每个单元格内每个段落的内容。
index = 0
for node in node_list:
    print(f'Table paragraph index {index}, contents: "{node.get_text().strip()}"')
    index += 1
# 此表达式将选择文档中任何 Body 节点的直接子段落。
node_list = doc.select_nodes('//Body/Paragraph')
# 我们可以把列表视为数组。
self.assertEqual(4, len(list(node_list)))
# 使用 SelectSingleNode 选择上述相同表达式的第一个结果。
node = doc.select_single_node('//Body/Paragraph')
self.assertEqual(aw.Paragraph, type(node.as_paragraph()))
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

