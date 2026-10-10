---
title: Revision class
linktitle: Revision class
articleTitle: Revision class
second_title: Aspose.Words for Python
description: "aspose.words.Revision class. Represents a revision (tracked change) in a document node or style"
type: docs
weight: 1050
url: /zh/python-net/aspose.words/revision/
---

## Revision class

Represents a revision (tracked change) in a document node or style.
Use [Revision.revision_type](./revision_type/) to check the type of this revision.
To learn more, visit the [Track Changes in a Document](https://docs.aspose.com/words/python-net/track-changes-in-a-document/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [author](./author/) | Gets or sets the author of this revision. Can not be empty string or ``None``. |
| [date_time](./date_time/) | Gets or sets the date/time of this revision. |
| [group](./group/) | Gets the revision group. Returns ``None`` if the revision does not belong to any group. |
| [parent_node](./parent_node/) | Gets the immediate parent node (owner) of this revision. This property will work for any revision type other than [RevisionType.STYLE_DEFINITION_CHANGE](../revisiontype/#STYLE_DEFINITION_CHANGE). |
| [parent_style](./parent_style/) | Gets the immediate parent style (owner) of this revision. This property will work for only for the [RevisionType.STYLE_DEFINITION_CHANGE](../revisiontype/#STYLE_DEFINITION_CHANGE) revision type. |
| [revision_type](./revision_type/) | Gets the type of this revision. |

### Methods

| Name | Description |
| --- | --- |
|[ accept()](./accept/#default) | Accepts this revision. |
|[ reject()](./reject/#default) | Reject this revision. |

### Examples

Shows how to work with revisions in a document.

```python
class ExRevision(ApiExampleBase):

    def test_revisions(self):
        doc = aw.Document()
        builder = aw.DocumentBuilder(doc=doc)
        # 对文档的普通编辑不计入修订。
        builder.write('This does not count as a revision. ')
        self.assertFalse(doc.has_revisions)
        # 要将我们的编辑注册为修订，需要声明作者，然后开始跟踪它们。
        doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
        builder.write('This is revision #1. ')
        self.assertTrue(doc.has_revisions)
        self.assertEqual(1, doc.revisions.count)
        # 此标志对应于 Microsoft Word 中的“审阅” -> “跟踪” -> “修订”选项。
        # “StartTrackRevisions” 方法不会影响其值，
        # 即使其值为“false”，文档仍会通过编程方式跟踪修订。
        # 如果我们使用 Microsoft Word 打开此文档，它将不会跟踪修订。
        self.assertFalse(doc.track_revisions)
        # 我们使用文档构建器添加了文本，因此第一次修订是插入类型的修订。
        revision = doc.revisions[0]
        self.assertEqual('John Doe', revision.author)
        self.assertEqual('This is revision #1. ', revision.parent_node.get_text())
        self.assertEqual(aw.RevisionType.INSERTION, revision.revision_type)
        self.assertEqual(revision.date_time.date(), datetime.datetime.now().date())
        self.assertEqual(doc.revisions.groups[0], revision.group)
        # 删除一个运行以创建删除类型的修订。
        doc.first_section.body.first_paragraph.runs[0].remove()
        # 添加新修订会将其放置在修订集合的开头。
        self.assertEqual(aw.RevisionType.DELETION, doc.revisions[0].revision_type)
        self.assertEqual(2, doc.revisions.count)
        # 插入修订会在我们接受/拒绝修订之前就显示在文档主体中。
        # 拒绝此修订将从正文中移除其节点。相反，构成删除修订的节点
        # 也会在文档中保留，直到我们接受该修订。
        self.assertEqual('This does not count as a revision. This is revision #1.', doc.get_text().strip())
        # 接受删除修订将从段落文本中移除其父节点
        # 随后移除集合本身的修订。
        doc.revisions[0].accept()
        self.assertEqual(1, doc.revisions.count)
        self.assertEqual('This is revision #1.', doc.get_text().strip())
        builder.writeln('')
        builder.write('This is revision #2.')
        # 现在移动该节点以创建移动修订类型。
        node = doc.first_section.body.paragraphs[1]
        end_node = doc.first_section.body.paragraphs[1].next_sibling
        reference_node = doc.first_section.body.paragraphs[0]
        while node != end_node:
            next_node = node.next_sibling
            doc.first_section.body.insert_before(node, reference_node)
            node = next_node
        self.assertEqual(aw.RevisionType.MOVING, doc.revisions[0].revision_type)
        self.assertEqual(8, doc.revisions.count)
        self.assertEqual('This is revision #2.\rThis is revision #1. \rThis is revision #2.', doc.get_text().strip())
        # 移动修订现在位于索引 1。拒绝该修订以丢弃其内容。
        doc.revisions[1].reject()
        self.assertEqual(6, doc.revisions.count)
        self.assertEqual('This is revision #1. \rThis is revision #2.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../)

