---
title: ParagraphCollection indexer
linktitle: ParagraphCollection indexer
articleTitle: ParagraphCollection indexer
second_title: Aspose.Words for Python
description: "ParagraphCollection indexer. Retrieves a [Paragraph](../../paragraph/) at the given index."
type: docs
weight: 10
url: /ru/python-net/aspose.words/paragraphcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [Paragraph](../../paragraph/) at the given index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




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
* class [ParagraphCollection](../)

