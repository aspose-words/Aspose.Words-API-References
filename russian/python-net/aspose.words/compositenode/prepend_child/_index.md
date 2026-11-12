---
title: CompositeNode.prepend_child method
linktitle: prepend_child method
articleTitle: prepend_child method
second_title: Aspose.Words for Python
description: "CompositeNode.prepend_child method. Adds the specified node to the beginning of the list of child nodes for this node."
type: docs
weight: 150
url: /ru/python-net/aspose.words/compositenode/prepend_child/
---

## prepend_child(new_child) {#node}

Adds the specified node to the beginning of the list of child nodes for this node.


```python
def prepend_child(self, new_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_child | [Node](../../node/) | The node to add. |

### Remarks

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The node added.


### Examples

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```python
doc = aw.Document()
# Пустой документ по умолчанию содержит один абзац.
self.assertEqual(1, doc.first_section.body.paragraphs.count)
# Составные узлы, такие как наш абзац, могут содержать другие составные и встроенные узлы как дочерние.
paragraph = doc.first_section.body.first_paragraph
paragraph_text = aw.Run(doc=doc, text='Initial text. ')
paragraph.append_child(paragraph_text)
# Создайте ещё три узла run.
run1 = aw.Run(doc=doc, text='Run 1. ')
run2 = aw.Run(doc=doc, text='Run 2. ')
run3 = aw.Run(doc=doc, text='Run 3. ')
# Тело документа не будет отображать эти runs, пока мы не вставим их в составной узел
# который сам является частью дерева узлов документа, как мы сделали с первым run.
# Мы можем определить, где будет находиться текстовое содержимое узлов, которые мы вставляем
# появляется в документе, указывая место вставки относительно другого узла в абзаце.
self.assertEqual('Initial text.', paragraph.get_text().strip())
# Вставьте второй run в абзац перед начальным run.
paragraph.insert_before(run2, paragraph_text)
self.assertEqual('Run 2. Initial text.', paragraph.get_text().strip())
# Вставьте третий run после начального run.
paragraph.insert_after(run3, paragraph_text)
self.assertEqual('Run 2. Initial text. Run 3.', paragraph.get_text().strip())
# Вставьте первый run в начало коллекции дочерних узлов абзаца.
paragraph.prepend_child(run1)
self.assertEqual('Run 1. Run 2. Initial text. Run 3.', paragraph.get_text().strip())
self.assertEqual(4, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
# Мы можем изменить содержимое run, редактируя и удаляя существующие дочерние узлы.
paragraph.get_child_nodes(aw.NodeType.RUN, True)[1].as_run().text = 'Updated run 2. '
paragraph.get_child_nodes(aw.NodeType.RUN, True).remove(paragraph_text)
self.assertEqual('Run 1. Updated run 2. Run 3.', paragraph.get_text().strip())
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

