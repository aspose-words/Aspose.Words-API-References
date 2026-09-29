---
title: CompositeNode.select_nodes method
linktitle: select_nodes method
articleTitle: select_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.select_nodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 190
url: /tr/python-net/aspose.words/compositenode/select_nodes/
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
# Bu ifade tüm paragraf düğümlerini çıkaracaktır,
# ki bunlar belgedeki herhangi bir tablo düğümünün alt öğeleridir.
node_list = doc.select_nodes('//Table//Paragraph')
# Listeyi bir enumerator ile yineleyin ve tablonun her hücresindeki her paragrafın içeriğini yazdırın.
index = 0
for node in node_list:
    print(f'Table paragraph index {index}, contents: "{node.get_text().strip()}"')
    index += 1
# Bu ifade, belgedeki herhangi bir Body düğümünün doğrudan alt öğesi olan tüm paragrafları seçecektir.
node_list = doc.select_nodes('//Body/Paragraph')
# Listeyi bir dizi gibi ele alabiliriz.
self.assertEqual(4, len(list(node_list)))
# SelectSingleNode'u kullanarak yukarıdaki aynı ifadenin ilk sonucunu seçin.
node = doc.select_single_node('//Body/Paragraph')
self.assertEqual(aw.Paragraph, type(node.as_paragraph()))
```

Shows how to use an XPath expression to test whether a node is inside a field.

```python
doc = aw.Document(file_name=MY_DIR + 'Mail merge destination - Northwind employees.docx')
# Bu XPath ifadesinden elde edilen NodeList, bir alan içinde bulduğumuz tüm düğümleri içerecektir.
# Ancak, yolda iç içe alanlar varsa FieldStart ve FieldEnd düğümleri listede bulunabilir.
# Şu anda, FieldCode veya FieldResult'un birden fazla paragrafı kapsadığı nadir alanları bulamıyor.
result_list = doc.select_nodes('//FieldStart/following-sibling::node()[following-sibling::FieldEnd]')
# Belirtilen çalıştırmanın alanın içinde bulunan düğümlerden biri olup olmadığını kontrol edin.
first_run = next((n for n in result_list if n.node_type == aw.NodeType.RUN), None)
if first_run:
    print(f"Contents of the first Run node that's part of a field: {first_run.get_text().strip()}")
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

