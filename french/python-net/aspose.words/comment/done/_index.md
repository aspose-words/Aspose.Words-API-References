---
title: Comment.done property
linktitle: done property
articleTitle: done property
second_title: Aspose.Words for Python
description: "Comment.done property. Gets or sets flag indicating that the comment has been marked done."
type: docs
weight: 60
url: /fr/python-net/aspose.words/comment/done/
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
# Insérez un commentaire pour signaler une erreur.
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('Fix the spelling error!')
doc.first_section.body.first_paragraph.append_child(comment)
# Les commentaires ont un drapeau "Done", qui est réglé sur "false" par défaut.
# Si un commentaire suggère que nous apportions une modification dans le document,
# nous pouvons appliquer la modification, puis également définir le drapeau "Done" par la suite pour indiquer la correction.
self.assertFalse(comment.done)
doc.first_section.body.first_paragraph.runs[0].text = 'Hello world!'
comment.done = True
# Les commentaires qui sont "done" se différencieront
# des commentaires qui ne sont pas "done" avec une couleur de texte atténuée.
comment = aw.Comment(doc=doc, author='John Doe', initial='J.D.', date_time=datetime.datetime.now())
comment.set_text('Add text to this paragraph.')
builder.current_paragraph.append_child(comment)
doc.save(file_name=ARTIFACTS_DIR + 'Comment.Done.docx')
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

