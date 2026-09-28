---
title: Comment.done property
linktitle: done property
articleTitle: done property
second_title: Aspose.Words for Python
description: "Comment.done property. Gets or sets flag indicating that the comment has been marked done."
type: docs
weight: 60
url: /de/python-net/aspose.words/comment/done/
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
# Füge einen Kommentar ein, um einen Fehler hervorzuheben.
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('Fix the spelling error!')
doc.first_section.body.first_paragraph.append_child(comment)
# Kommentare haben ein "Done"-Flag, das standardmäßig auf "false" gesetzt ist.
# Wenn ein Kommentar vorschlägt, dass wir eine Änderung im Dokument vornehmen,
# können wir die Änderung anwenden und anschließend das "Done"-Flag setzen, um die Korrektur anzuzeigen.
self.assertFalse(comment.done)
doc.first_section.body.first_paragraph.runs[0].text = 'Hello world!'
comment.done = True
# Kommentare, die "done" sind, unterscheiden sich
# von denen, die nicht "done" sind, durch eine verblasste Textfarbe.
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('Add text to this paragraph.')
builder.current_paragraph.append_child(comment)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.Done.docx')
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

