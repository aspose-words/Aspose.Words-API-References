---
title: DocumentBuilder.is_at_end_of_paragraph property
linktitle: is_at_end_of_paragraph property
articleTitle: is_at_end_of_paragraph property
second_title: Aspose.Words for Python
description: "DocumentBuilder.is_at_end_of_paragraph property. Returns ``True`` if the cursor is at the end of the current paragraph."
type: docs
weight: 110
url: /tr/python-net/aspose.words/documentbuilder/is_at_end_of_paragraph/
---

## DocumentBuilder.is_at_end_of_paragraph property

Returns ``True`` if the cursor is at the end of the current paragraph.



```python
@property
def is_at_end_of_paragraph(self) -> bool:
    ...

```

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

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

