---
title: Node.parent_node property
linktitle: parent_node property
articleTitle: parent_node property
second_title: Aspose.Words for Python
description: "Node.parent_node property. Gets the immediate parent of this node."
type: docs
weight: 60
url: /ru/python-net/aspose.words/node/parent_node/
---

## Node.parent_node property

Gets the immediate parent of this node.


```python
@property
def parent_node(self) -> aspose.words.CompositeNode:
    ...

```

### Remarks

If a node has just been created and not yet added to the tree,
or if it has been removed from the tree, the parent is ``None``.




### Examples

Shows how to create a node and set its owning document.

```python
from api_example_base import ApiExampleBase
doc = aw.Document()
para = aw.Paragraph(doc)
para.append_child(aw.Run(doc=doc, text='Hello world!'))
# Мы ещё не добавили этот абзац как дочерний элемент к какому-либо составному узлу.
self.assertIsNone(para.parent_node)
# Если узел является подходящим типом дочернего узла другого составного узла,
# мы можем присоединить его как дочерний элемент только если оба узла имеют один и тот же документ‑владелец.
# Документ‑владелец — это документ, который мы передали в конструктор узла.
# Мы не прикрепили этот абзац к документу, поэтому документ не содержит его текста.
self.assertEqual(para.document, doc)
self.assertEqual('', doc.get_text().strip())
# Поскольку документ владеет этим абзацем, мы можем применить один из его стилей к содержимому абзаца.
para.paragraph_format.style = doc.styles.get_by_name('Heading 1')
# Добавьте этот узел в документ, а затем проверьте его содержимое.
doc.first_section.body.append_child(para)
self.assertEqual(doc.first_section.body, para.parent_node)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

