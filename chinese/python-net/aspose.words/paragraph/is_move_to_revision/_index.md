---
title: Paragraph.is_move_to_revision property
linktitle: is_move_to_revision property
articleTitle: is_move_to_revision property
second_title: Aspose.Words for Python
description: "Paragraph.is_move_to_revision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 140
url: /zh/python-net/aspose.words/paragraph/is_move_to_revision/
---

## Paragraph.is_move_to_revision property

Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_to_revision(self) -> bool:
    ...

```

### Examples

Shows how to check whether a paragraph is a move revision.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# 此文档包含 "Move" 修订，当我们使用光标突出显示文本时会出现，
# 然后拖动它以将其移动到其他位置
# 在 Microsoft Word 中通过 "Review" -> "Track changes" 跟踪修订时。
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# Move 修订由 "Move from" 和 "Move to" 修订对组成。
# 这些修订是文档的潜在更改，我们可以接受或拒绝它们。
# 在我们接受/拒绝移动修订之前，文档
# 必须跟踪文本的出发和到达位置。
# 第二段和第四段定义了这样的一个修订，因此两者具有相同的内容。
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# "Move from" 修订是我们拖动文本的段落。
# 如果我们接受该修订，此段落将消失，
# 而另一个将保留且不再是修订。
self.assertTrue(paragraphs[1].is_move_from_revision)
# "Move to" 修订是我们将文本拖动到的段落。
# 如果我们拒绝该修订，此段落将消失，而另一个将保留。
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

