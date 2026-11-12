---
title: Story.paragraphs property
linktitle: paragraphs property
articleTitle: paragraphs property
second_title: Aspose.Words for Python
description: "Story.paragraphs property. Gets a collection of paragraphs that are immediate children of the story."
type: docs
weight: 30
url: /ru/python-net/aspose.words/story/paragraphs/
---

## Story.paragraphs property

Gets a collection of paragraphs that are immediate children of the story.


```python
@property
def paragraphs(self) -> aspose.words.ParagraphCollection:
    ...

```

### Examples

Shows how to check whether a paragraph is a move revision.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# Этот документ содержит правки "Move", которые появляются, когда мы выделяем текст курсором,
# а затем перетаскиваем его, чтобы переместить в другое место
# при отслеживании правок в Microsoft Word через "Review" -> "Track changes".
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# Правки перемещения состоят из пар правок "Move from" и "Move to".
# Эти правки являются потенциальными изменениями документа, которые мы можем либо принять, либо отклонить.
# Прежде чем мы примем/отклоним правку перемещения, документ
# должен отслеживать как исходные, так и конечные места текста.
# Второй и четвертый абзацы определяют одну такую правку, поэтому оба имеют одинаковое содержание.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# Правка "Move from" — это абзац, из которого мы перетаскивали текст.
# Если мы примем правку, этот абзац исчезнет,
# а другой останется и больше не будет правкой.
self.assertTrue(paragraphs[1].is_move_from_revision)
# Правка "Move to" — это абзац, в который мы перетаскивали текст.
# Если мы отклоним правку, вместо этого исчезнет этот абзац, а другой останется.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

