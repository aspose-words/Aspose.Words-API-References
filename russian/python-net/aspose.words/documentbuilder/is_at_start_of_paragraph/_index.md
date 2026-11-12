---
title: DocumentBuilder.is_at_start_of_paragraph property
linktitle: is_at_start_of_paragraph property
articleTitle: is_at_start_of_paragraph property
second_title: Aspose.Words for Python
description: "DocumentBuilder.is_at_start_of_paragraph property. Returns ``True`` if the cursor is at the beginning of the current paragraph (no text before the cursor)."
type: docs
weight: 130
url: /ru/python-net/aspose.words/documentbuilder/is_at_start_of_paragraph/
---

## DocumentBuilder.is_at_start_of_paragraph property

Returns ``True`` if the cursor is at the beginning of the current paragraph (no text before the cursor).



```python
@property
def is_at_start_of_paragraph(self) -> bool:
    ...

```

### Examples

Shows how to move a document builder's cursor to different nodes in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создать действительную закладку, объект, состоящий из узлов, заключённых между начальным узлом закладки,
# и конечным узлом закладки.
builder.start_bookmark('MyBookmark')
builder.write('Bookmark contents.')
builder.end_bookmark('MyBookmark')
first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual('Bookmark contents.', first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)
# Курсор построителя документа всегда находится впереди узла, который мы последним добавили с его помощью.
# Если курсор построителя находится в конце документа, его текущий узел будет равен null.
# Предыдущий узел — это конечный узел закладки, который мы последним добавили.
# Добавление новых узлов с помощью построителя присоединит их к последнему узлу.
self.assertIsNone(builder.current_node)
# Если мы хотим отредактировать другую часть документа с помощью построителя,
# нам потребуется переместить его курсор к узлу, который мы хотим отредактировать.
builder.move_to_bookmark(bookmark_name='MyBookmark')
# Перемещение его к закладке переместит его к первому узлу внутри начального и конечного узлов закладки, заключённому фрагменту.
self.assertEqual(first_paragraph_nodes[1], builder.current_node)
# Мы также можем переместить курсор к отдельному узлу следующим образом.
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])
self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)
# Мы можем использовать специальные методы для перемещения к началу/концу документа.
builder.move_to_document_end()
self.assertTrue(builder.is_at_end_of_paragraph)
builder.move_to_document_start()
self.assertTrue(builder.is_at_start_of_paragraph)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

