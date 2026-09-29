---
title: DocumentBuilder.move_to method
linktitle: move_to method
articleTitle: move_to method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 520
url: /tr/python-net/aspose.words/documentbuilder/move_to/
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
# Geçerli bir yer imi oluştur, bu, bir yer imi başlangıç düğümüyle çevrili düğümlerden oluşan bir varlıktır,
# ve bir yer imi bitiş düğümü.
builder.start_bookmark('MyBookmark')
builder.write('Bookmark contents.')
builder.end_bookmark('MyBookmark')
first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual('Bookmark contents.', first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)
# Belge oluşturucunun imleci, onunla en son eklediğimiz düğümün her zaman önündedir.
# Eğer oluşturucunun imleci belgenin sonunda ise, mevcut düğümü null olacaktır.
# Önceki düğüm, en son eklediğimiz yer imi bitiş düğümüdür.
# Oluşturucu ile yeni düğümler eklemek, onları son düğüme ekleyecektir.
self.assertIsNone(builder.current_node)
# Eğer oluşturucu ile belgenin farklı bir bölümünü düzenlemek istersek,
# imlecini düzenlemek istediğimiz düğüme getirmemiz gerekir.
builder.move_to_bookmark(bookmark_name='MyBookmark')
# Bunu bir yer imine taşımak, onu yer imi başlangıç ve bitiş düğümleri arasındaki ilk düğüme, yani kapsanan çalışmaya taşıyacaktır.
self.assertEqual(first_paragraph_nodes[1], builder.current_node)
# İmleci bu şekilde tek bir düğüme de taşıyabiliriz.
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])
self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)
# Belgenin başlangıç/bitimine gitmek için belirli yöntemler kullanabiliriz.
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
# Belge oluşturucu bir imlece sahiptir; bu imleç belgenin bir bölümü gibi davranır
# yapıcı, belge oluşturma yöntemlerini kullandığımızda yeni düğümler eklediği yerdir.
# Bu imleç, Microsoft Word'ün yanıp sönen imleciyle aynı şekilde çalışır,
# ve ayrıca her zaman yapıcının yeni eklediği herhangi bir düğümün hemen sonrasında bulunur.
# Belgenin farklı bir bölümüne içerik eklemek için,
# imleci \"MoveTo\" yöntemiyle farklı bir düğüme taşıyabiliriz.
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# İmleç şimdi taşındığı düğümün önündedir.
# İkinci bir çalışmanın eklenmesi, onu ilk çalışmanın önüne yerleştirir.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# İmleci belgenin sonuna taşıyarak, daha önceki gibi metni sona eklemeye devam edin.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

