---
title: CommentCollection class
linktitle: CommentCollection class
articleTitle: CommentCollection class
second_title: Aspose.Words for Python
description: "aspose.words.CommentCollection class. Provides typed access to a collection of [Comment](../comment/) nodes"
type: docs
weight: 190
url: /zh/python-net/aspose.words/commentcollection/
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
# 插入评论以指出错误。
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('Fix the spelling error!')
doc.first_section.body.first_paragraph.append_child(comment)
# 评论具有一个 "Done" 标志，默认设置为 "false"。
# 如果评论建议我们在文档中进行更改，
# 我们可以应用更改，然后随后设置 "Done" 标志以表明已纠正。
self.assertFalse(comment.done)
doc.first_section.body.first_paragraph.runs[0].text = 'Hello world!'
comment.done = True
# 标记为 "done" 的评论将自行区分
# 与未标记为 "done" 的评论使用淡化的文字颜色区别开来。
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('Add text to this paragraph.')
builder.current_paragraph.append_child(comment)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.Done.docx')
```

### See Also

* module [aspose.words](../)
* class [NodeCollection](../nodecollection/)

