---
title: CompositeNode.select_single_node method
linktitle: select_single_node method
articleTitle: select_single_node method
second_title: Aspose.Words for Python
description: "CompositeNode.select_single_node method. Selects the first [Node](../../node/) that matches the XPath expression."
type: docs
weight: 200
url: /ar/python-net/aspose.words/compositenode/select_single_node/
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
# هذا التعبير سيستخرج جميع عقد الفقرة paragraph nodes،
# والتي هي من سلالات أي عقدة جدول table في المستند.
node_list = doc.select_nodes('//Table//Paragraph')
# تجول عبر القائمة باستخدام enumerator واطبع محتويات كل فقرة في كل خلية من الجدول table.
index = 0
for node in node_list:
    print(f'Table paragraph index {index}, contents: "{node.get_text().strip()}"')
    index += 1
# هذا التعبير سيختار أي فقرات هي أبناء مباشرة لأي عقدة Body في المستند.
node_list = doc.select_nodes('//Body/Paragraph')
# يمكننا اعتبار القائمة كمصفوفة.
self.assertEqual(4, len(list(node_list)))
# استخدم SelectSingleNode لاختيار النتيجة الأولى لنفس التعبير أعلاه.
node = doc.select_single_node('//Body/Paragraph')
self.assertEqual(aw.Paragraph, type(node.as_paragraph()))
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

