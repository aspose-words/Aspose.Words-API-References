---
title: NodeList.to_array method
linktitle: to_array method
articleTitle: to_array method
second_title: Aspose.Words for Python
description: "NodeList.to_array method. Copies all nodes from the collection to a new array of nodes."
type: docs
weight: 30
url: /ru/python-net/aspose.words/nodelist/to_array/
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
# Это выражение извлечёт все узлы абзацев,
# которые являются потомками любого узла таблицы в документе.
node_list = doc.select_nodes('//Table//Paragraph')
# Итерируйте список с помощью перечислителя и выводите содержимое каждого абзаца в каждой ячейке таблицы.
index = 0
for node in node_list:
    print(f'Table paragraph index {index}, contents: "{node.get_text().strip()}"')
    index += 1
# Это выражение выберет любые абзацы, являющиеся прямыми дочерними элементами любого узла Body в документе.
node_list = doc.select_nodes('//Body/Paragraph')
# Мы можем рассматривать список как массив.
self.assertEqual(4, len(list(node_list)))
# Используйте SelectSingleNode, чтобы выбрать первый результат того же выражения, что выше.
node = doc.select_single_node('//Body/Paragraph')
self.assertEqual(aw.Paragraph, type(node.as_paragraph()))
```

### See Also

* module [aspose.words](../../)
* class [NodeList](../)

