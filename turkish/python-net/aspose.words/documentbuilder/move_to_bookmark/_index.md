---
title: DocumentBuilder.move_to_bookmark method
linktitle: move_to_bookmark method
articleTitle: move_to_bookmark method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.move_to_bookmark method"
type: docs
weight: 530
url: /tr/python-net/aspose.words/documentbuilder/move_to_bookmark/
---

## move_to_bookmark(bookmark_name) {#str}

Moves the cursor to a bookmark.


```python
def move_to_bookmark(self, bookmark_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmark_name | str | The name of the bookmark to move the cursor to. |

### Remarks

Moves the cursor to a position just after the start of the bookmark with the
specified name.

The comparison is not case-sensitive. If the bookmark was not found, ``False`` is
returned and the cursor is not moved.

Inserting new text does not replace existing text of the bookmark.

Note that some bookmarks in the document are assigned to form fields.
Moving to such a bookmark and inserting text there inserts the text into the
form field code. Although this will not invalidate the form field, the inserted
text will not be visible because it becomes part of the field code.




### Returns

``True`` if the bookmark was found; ``False`` otherwise.


## move_to_bookmark(bookmark_name, is_start, is_after) {#str_bool_bool}

Moves the cursor to a bookmark with greater precision.


```python
def move_to_bookmark(self, bookmark_name: str, is_start: bool, is_after: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmark_name | str | The name of the bookmark to move the cursor to. |
| is_start | bool | When ``True``, moves the cursor to the beginning of the bookmark. When ``False``, moves the cursor to the end of the bookmark. |
| is_after | bool | When ``True``, moves the cursor to be after the bookmark start or end position. When ``False``, moves the cursor to be before the bookmark start or end position. |

### Remarks

Moves the cursor to a position before or after the bookmark start or end.

If desired position is not at inline level, moves to the next paragraph.

The comparison is not case-sensitive. If the bookmark was not found, ``False`` is
returned and the cursor is not moved.




### Returns

``True`` if the bookmark was found; ``False`` otherwise.


## Examples

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

Shows how to move a document builder's node insertion point cursor to a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Geçerli bir yer işareti, bir BookmarkStart düğümü, bir BookmarkEnd düğümü ve
# daha sonra bir yerde eşleşen yer işareti adı ve bu düğümler tarafından kapsanan içerik.
builder.start_bookmark('MyBookmark')
builder.write('Hello world! ')
builder.end_bookmark('MyBookmark')
# Bir belge oluşturucusunun imlecini bir yer işaretine taşımanın 4 yolu vardır.
# BookmarkStart ve BookmarkEnd düğümleri arasında ise, imleç yer işaretinin içinde olacaktır.
# Bu, oluşturucu tarafından eklenen herhangi bir metnin yer işaretinin bir parçası olacağı anlamına gelir.
# 1 -  Yer işaretinin dışında, BookmarkStart düğümünün önünde:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=True, is_after=False))
builder.write('1. ')
self.assertEqual('Hello world! ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. Hello world!', doc.get_text().strip())
# 2 -  Yer işaretinin içinde, BookmarkStart düğümünden hemen sonra:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=True, is_after=True))
builder.write('2. ')
self.assertEqual('2. Hello world! ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world!', doc.get_text().strip())
# 2 -  Yer işaretinin içinde, BookmarkEnd düğümünün hemen önünde:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=False, is_after=False))
builder.write('3. ')
self.assertEqual('2. Hello world! 3. ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world! 3.', doc.get_text().strip())
# 4 -  Yer işaretinin dışında, BookmarkEnd düğümünden sonra:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=False, is_after=True))
builder.write('4.')
self.assertEqual('2. Hello world! 3. ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world! 3. 4.', doc.get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

