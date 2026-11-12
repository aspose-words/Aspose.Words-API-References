---
title: Section.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Section.ensure_minimum method. Ensures that the section has [Section.body](../body/) with one [Paragraph](../../paragraph/)."
type: docs
weight: 130
url: /ru/python-net/aspose.words/section/ensure_minimum/
---

## ensure_minimum() {#default}

Ensures that the section has [Section.body](../body/) with one [Paragraph](../../paragraph/).



```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to prepare a new section node for editing.

```python
doc = aw.Document()
# Пустой документ содержит раздел, который имеет тело, который, в свою очередь, имеет абзац.
# Мы можем добавить содержимое в этот документ, добавляя такие элементы, как текстовые run'ы, фигуры или таблицы, в этот абзац.
self.assertEqual(aw.NodeType.SECTION, doc.get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.BODY, doc.sections[0].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[0].body.get_child(aw.NodeType.ANY, 0, True).node_type)
# Если мы добавим новый раздел таким образом, у него не будет тела или каких-либо других дочерних узлов.
doc.sections.add(aw.Section(doc))
self.assertEqual(0, doc.sections[1].get_child_nodes(aw.NodeType.ANY, True).count)
# Вызовите метод "EnsureMinimum", чтобы добавить тело и абзац в этот раздел и начать его редактирование.
doc.last_section.ensure_minimum()
self.assertEqual(aw.NodeType.BODY, doc.sections[1].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[1].body.get_child(aw.NodeType.ANY, 0, True).node_type)
doc.sections[0].body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

