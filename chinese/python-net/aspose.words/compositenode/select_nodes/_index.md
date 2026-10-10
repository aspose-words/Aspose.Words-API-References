---
title: CompositeNode.select_nodes method
linktitle: select_nodes method
articleTitle: select_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.select_nodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 190
url: /zh/python-net/aspose.words/compositenode/select_nodes/
---

## select_nodes(xpath) {#str}

Selects a list of nodes matching the XPath expression.


```python
def select_nodes(self, xpath: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| xpath | str | The XPath expression. |

### Remarks

Only expressions with element names are supported at the moment. Expressions
that use attribute names are not supported.




### Returns

A list of nodes matching the XPath query.


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

Shows how to use an XPath expression to test whether a node is inside a field.

```python
doc = aw.Document(file_name=MY_DIR + 'Mail merge destination - Northwind employees.docx')
# 此 XPath 表达式产生的 NodeList 将包含我们在字段内部找到的所有节点。
# 然而，如果路径中存在嵌套字段，FieldStart 和 FieldEnd 节点也可能出现在列表中。
# 当前无法找到跨越多个段落的 FieldCode 或 FieldResult 的罕见字段。
result_list = doc.select_nodes('//FieldStart/following-sibling::node()[following-sibling::FieldEnd]')
# 检查指定的 run 是否是字段内部的节点之一。
first_run = next((n for n in result_list if n.node_type == aw.NodeType.RUN), None)
if first_run:
    print(f"Contents of the first Run node that's part of a field: {first_run.get_text().strip()}")
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

