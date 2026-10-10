---
title: CompositeNode.select_nodes method
linktitle: select_nodes method
articleTitle: select_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.select_nodes method. Selects a list of nodes matching the XPath expression."
type: docs
weight: 190
url: /ar/python-net/aspose.words/compositenode/select_nodes/
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

Shows how to use an XPath expression to test whether a node is inside a field.

```python
doc = aw.Document(file_name=MY_DIR + 'Mail merge destination - Northwind employees.docx')
# قائمة NodeList الناتجة عن هذا التعبير XPath ستحتوي على جميع العقد التي نجدها داخل حقل.
# مع ذلك، يمكن أن تكون عقد FieldStart و FieldEnd في القائمة إذا كان هناك حقول متداخلة في المسار.
# حاليًا لا يتم العثور على الحقول النادرة التي يمتد فيها FieldCode أو FieldResult عبر فقرات متعددة.
result_list = doc.select_nodes('//FieldStart/following-sibling::node()[following-sibling::FieldEnd]')
# تحقق مما إذا كان التشغيل المحدد أحد العقد الموجودة داخل الحقل.
first_run = next((n for n in result_list if n.node_type == aw.NodeType.RUN), None)
if first_run:
    print(f"Contents of the first Run node that's part of a field: {first_run.get_text().strip()}")
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

