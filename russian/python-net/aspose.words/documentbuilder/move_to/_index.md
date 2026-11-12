---
title: DocumentBuilder.move_to method
linktitle: move_to method
articleTitle: move_to method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 520
url: /ru/python-net/aspose.words/documentbuilder/move_to/
---

## move_to(node) {#node}

Moves the cursor to an inline node or to the end of a paragraph.


```python
def move_to(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node must be a paragraph or a direct child of a paragraph. |

### Remarks

When *node* is an inline-level node, the cursor is moved to this node
and further content will be inserted before that node.

When *node* is a [Paragraph](../../paragraph/), the cursor is moved to the end of the paragraph
and further content will be inserted just before the paragraph break.

When *node* is a block-level node but not a [Paragraph](../../paragraph/), the cursor is moved to the end of the first paragraph into block-level node
and further content will be inserted just before the paragraph break.




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

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# У конструктора документа есть курсор, который выступает как часть документа
# куда конструктор добавляет новые узлы, когда мы используем его методы построения документа.
# Этот курсор работает так же, как мигающий курсор Microsoft Word,
# и он также всегда оказывается сразу после любого узла, который конструктор только что вставил.
# Чтобы добавить содержимое в другую часть документа,
# мы можем переместить курсор к другому узлу с помощью метода "MoveTo".
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# Курсор теперь находится перед узлом, к которому мы его переместили.
# Добавление второго фрагмента вставит его перед первым фрагментом.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Переместите курсор в конец документа, чтобы продолжить добавлять текст в конец, как и раньше.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

