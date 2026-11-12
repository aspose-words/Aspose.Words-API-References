---
title: SectionCollection indexer
linktitle: SectionCollection indexer
articleTitle: SectionCollection indexer
second_title: Aspose.Words for Python
description: "SectionCollection indexer. Retrieves a section at the given index."
type: docs
weight: 10
url: /ru/python-net/aspose.words/sectioncollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a section at the given index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows when to recalculate the page layout of the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Сохранение документа в PDF, в изображение или печать в первый раз будет автоматически
# кешировать макет документа внутри его страниц.
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.1.pdf')
# Измените документ каким-либо образом.
doc.styles.get_by_name('Normal').font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE
doc.sections[0].page_setup.margins = aw.Margins.MIRRORED
# В текущей версии Aspose.Words изменение документа не приводит к автоматическому пересозданию
# кешированного макета страниц. Если мы хотим, чтобы кешированный макет
# оставался актуальным, нам придётся обновлять его вручную.
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.2.pdf')
```

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
* class [SectionCollection](../)

