---
title: CommentCollection class
linktitle: CommentCollection class
articleTitle: CommentCollection class
second_title: Aspose.Words for Python
description: "aspose.words.CommentCollection class. Provides typed access to a collection of [Comment](../comment/) nodes"
type: docs
weight: 190
url: /tr/python-net/aspose.words/commentcollection/
---

## CommentCollection class

Provides typed access to a collection of [Comment](../comment/) nodes.
To learn more, visit the [Working with Comments](https://docs.aspose.com/words/python-net/working-with-comments/) documentation article.




**Inheritance:** [CommentCollection](./) → [NodeCollection](../nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Comment](../comment/) at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ index_of(node)](../nodecollection/index_of/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#int_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove_at(index)](../nodecollection/remove_at/#int) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ to_array()](../nodecollection/to_array/#default) | Copies all nodes from the collection to a new array of nodes.<br>(Inherited from [NodeCollection](../nodecollection/)) |

### Examples

Shows how to mark a comment as "done".

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Helo world!')
# Hata göstermek için bir yorum ekleyin.
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('Fix the spelling error!')
doc.first_section.body.first_paragraph.append_child(comment)
# Yorumların bir "Done" bayrağı vardır ve varsayılan olarak "false" olarak ayarlanır.
# Eğer bir yorum, belgede bir değişiklik yapmamızı öneriyorsa,
# değişikliği uygulayabilir ve ardından düzeltmeyi göstermek için "Done" bayrağını ayarlayabiliriz.
self.assertFalse(comment.done)
doc.first_section.body.first_paragraph.runs[0].text = 'Hello world!'
comment.done = True
# "Done" olan yorumlar kendilerini farklılaştıracaktır
# "Done" olmayanlardan soluk bir metin rengiyle.
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('Add text to this paragraph.')
builder.current_paragraph.append_child(comment)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.Done.docx')
```

### See Also

* module [aspose.words](../)
* class [NodeCollection](../nodecollection/)

