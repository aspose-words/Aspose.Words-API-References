---
title: Comment.done property
linktitle: done property
articleTitle: done property
second_title: Aspose.Words for Python
description: "Comment.done property. Gets or sets flag indicating that the comment has been marked done."
type: docs
weight: 60
url: /zh/python-net/aspose.words/comment/done/
---

## Comment.done property

Gets or sets flag indicating that the comment has been marked done.


```python
@property
def done(self) -> bool:
    ...

@done.setter
def done(self, value: bool):
    ...

```

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

* module [aspose.words](../../)
* class [Comment](../)

