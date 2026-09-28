---
title: NodeCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "NodeCollection.remove method. Removes the node from the collection and from the document."
type: docs
weight: 80
url: /zh/python-net/aspose.words/nodecollection/remove/
---

## remove(node) {#node}

Removes the node from the collection and from the document.


```python
def remove(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node to remove. |

### Examples

Shows how to work with a NodeCollection.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 使用 DocumentBuilder 插入 Run 来向文档添加文本。
builder.write('Run 1. ')
builder.write('Run 2. ')
# 每次调用 "Write" 方法都会创建一个新的 Run，
# 随后它会出现在父 Paragraph 的 RunCollection 中。
runs = doc.first_section.body.first_paragraph.runs
self.assertEqual(2, runs.count)
# 我们也可以手动向 RunCollection 插入节点。
new_run = aw.Run(doc=doc, text='Run 3. ')
runs.insert(3, new_run)
self.assertTrue(runs.contains(new_run))
self.assertEqual('Run 1. Run 2. Run 3.', doc.get_text().strip())
# 访问各个 Run 并将其移除，以从文档中删除其文本。
run = runs[1]
runs.remove(run)
self.assertEqual('Run 1. Run 3.', doc.get_text().strip())
self.assertIsNotNone(run)
self.assertFalse(runs.contains(run))
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

