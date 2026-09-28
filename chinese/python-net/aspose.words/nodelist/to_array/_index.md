---
title: NodeList.to_array method
linktitle: to_array method
articleTitle: to_array method
second_title: Aspose.Words for Python
description: "NodeList.to_array method. Copies all nodes from the collection to a new array of nodes."
type: docs
weight: 30
url: /zh/python-net/aspose.words/nodelist/to_array/
---

## to_array() {#default}

Copies all nodes from the collection to a new array of nodes.


```python
def to_array(self):
    ...
```

### Remarks

You should not be adding/removing nodes while iterating over a collection 
of nodes because it invalidates the iterator and requires refreshes for live collections.

To be able to add/remove nodes during iteration, use this method to copy 
nodes into a fixed-size array and then iterate over the array.




### Returns

An array of nodes.


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
* class [NodeList](../)

