---
title: Revision.parent_style property
linktitle: parent_style property
articleTitle: parent_style property
second_title: Aspose.Words for Python
description: "Revision.parent_style property. Gets the immediate parent style (owner) of this revision"
type: docs
weight: 50
url: /zh/python-net/aspose.words/revision/parent_style/
---

## Revision.parent_style property

Gets the immediate parent style (owner) of this revision.
This property will work for only for the [RevisionType.STYLE_DEFINITION_CHANGE](../../revisiontype/#STYLE_DEFINITION_CHANGE) revision type.



```python
@property
def parent_style(self) -> aspose.words.Style:
    ...

```

### Remarks

If this revision relates to changes on document nodes, use [Revision.parent_node](../parent_node/) instead.



### Examples

Shows how to work with a document's collection of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
revisions = doc.revisions
# 此集合本身包含一个修订组的集合。
# 每个组都是相邻修订的序列。
group_count = sum((1 for _ in revisions.groups))
print(f'{group_count} revision groups:')
# 遍历组的集合并打印修订涉及的文本。
for group in revisions.groups:
    print(f'\tGroup type "{group.revision_type}", ' + f'author: {group.author}, contents: [{group.text.strip()}]')
# 每个受修订影响的 Run 都会获得相应的 Revision 对象。
# 修订集合明显大于我们上面打印的精简形式，
# 这取决于我们在 Microsoft Word 编辑期间将文档分割成了多少个 Run。
revision_count = sum((1 for _ in revisions))
print(f'\n{revision_count} revisions:')
for revision in revisions:
    # StyleDefinitionChange 仅影响样式而不影响文档节点。这意味着 "ParentStyle" 属性将始终被使用，而 ParentNode 将始终为 null。
    # 由于所有其他更改都会影响节点，ParentNode 将相应地被使用，而 ParentStyle 将为 null。
    if revision.revision_type == aw.RevisionType.STYLE_DEFINITION_CHANGE:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, style: [{revision.parent_style.name}]')
    else:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, contents: [{revision.parent_node.get_text().strip()}]')
# 通过集合拒绝所有修订，将文档恢复到原始形式。
revisions.reject_all()
self.assertEqual(0, sum((1 for _ in revisions)))
```

### See Also

* module [aspose.words](../../)
* class [Revision](../)

