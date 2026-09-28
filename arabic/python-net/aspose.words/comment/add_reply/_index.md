---
title: Comment.add_reply method
linktitle: add_reply method
articleTitle: add_reply method
second_title: Aspose.Words for Python
description: "Comment.add_reply method. Adds a reply to this comment."
type: docs
weight: 160
url: /ar/python-net/aspose.words/comment/add_reply/
---

## add_reply(author, initial, date_time, text) {#str_str_datetime_str}

Adds a reply to this comment.


```python
def add_reply(self, author: str, initial: str, date_time: datetime.datetime, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| author | str | The author name for the reply. |
| initial | str | The author initials for the reply. |
| date_time | datetime.datetime | The date and time for the reply. |
| text | str | The reply text. |

### Remarks

Due to the existing MS Office limitations only 1 level of replies is allowed in the document.




### Returns

The created [Comment](../) node for the reply.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throws if this method is called on the existing Reply comment. |

### Examples

Shows how to add a comment to a document, and then reply to it.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('My comment.')
# وضع التعليق عند عقدة في جسم المستند.
# سيظهر هذا التعليق في موقع الفقرة الخاصة به،
# خارج الهامش الأيمن للصفحة، ومع خط منقط يربطه بالفقرة.
builder.current_paragraph.append_child(comment)
# أضف ردًا، سيظهر تحت التعليق الأصلي.
comment.add_reply('Joe Bloggs', 'J.B.', datetime.datetime.now(), 'New reply')
# التعليقات والردود هي كلاهما عقدة تعليق.
self.assertEqual(2, doc.get_child_nodes(aw.NodeType.COMMENT, True).count)
# التعليقات التي لا ترد على تعليقات أخرى هي "عليا". ليس لديها تعليقات سلفية.
self.assertIsNone(comment.ancestor)
# الردود لها تعليق سلفي عليا.
self.assertEqual(comment, comment.replies[0].ancestor)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.AddCommentWithReply.docx')
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

