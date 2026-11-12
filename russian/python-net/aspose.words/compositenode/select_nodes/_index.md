---
title: CompositeNode.select_nodes method
linktitle: select_nodes method
articleTitle: select_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.select_nodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 190
url: /ru/python-net/aspose.words/compositenode/select_nodes/
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

Shows how to use an XPath expression to test whether a node is inside a field.

```python
doc = aw.Document(file_name=MY_DIR + 'Mail merge destination - Northwind employees.docx')
# NodeList, полученный в результате этого XPath-выражения, будет содержать все узлы, которые мы находим внутри поля.
# Однако узлы FieldStart и FieldEnd могут присутствовать в списке, если в пути есть вложенные поля.
# В настоящее время не находятся редкие поля, в которых FieldCode или FieldResult охватывают несколько абзацев.
result_list = doc.select_nodes('//FieldStart/following-sibling::node()[following-sibling::FieldEnd]')
# Проверьте, является ли указанный фрагмент одним из узлов, находящихся внутри поля.
first_run = next((n for n in result_list if n.node_type == aw.NodeType.RUN), None)
if first_run:
    print(f"Contents of the first Run node that's part of a field: {first_run.get_text().strip()}")
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

