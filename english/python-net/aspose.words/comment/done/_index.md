---
title: Comment.done property
linktitle: done property
articleTitle: done property
second_title: Aspose.Words for Python
description: "Comment.done property. Gets or sets flag indicating that the comment has been marked done."
type: docs
weight: 60
url: /python-net/aspose.words/comment/done/
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
builder = aw.DocumentBuilder(doc)
builder.writeln('Helo world!')
# Insert a comment to point out an error.
comment = aw.Comment(doc, 'John Doe', 'J.D.', datetime.now())
comment.set_text('Fix the spelling error!')
doc.first_section.body.first_paragraph.append_child(comment)
# Comments have a "done" flag, which is set to "False" by default.
# If a comment suggests that we make a change within the document,
# we can apply the change, and then also set the "done" flag afterwards to indicate the correction.
self.assertFalse(comment.done)
doc.first_section.body.first_paragraph.runs[0].text = 'Hello world!'
comment.done = True
# Comments that are "done" will differentiate themselves
# from ones that are not "done" with a faded text color.
comment = aw.Comment(doc, 'John Doe', 'J.D.', datetime.now())
comment.set_text('Add text to this paragraph.')
builder.current_paragraph.append_child(comment)
doc.save(ARTIFACTS_DIR + 'Comment.done.docx')
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

