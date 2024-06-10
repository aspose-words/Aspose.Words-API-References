---
title: Revision.parent_style property
linktitle: parent_style property
articleTitle: parent_style property
second_title: Aspose.Words for Python
description: "Revision.parent_style property. Gets the immediate parent style (owner) of this revision"
type: docs
weight: 50
url: /python-net/aspose.words/revision/parent_style/
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
doc = aw.Document(MY_DIR + 'Revisions.docx')
revisions = doc.revisions
# This collection itself has a collection of revision groups.
# Each group is a sequence of adjacent revisions.
print(revisions.groups.count, 'revision groups:')
# Iterate over the collection of groups and print the text that the revision concerns.
for group in revisions.groups:
    print(f'\tGroup type "{group.revision_type}", ' + f'author: {group.author}, contents: [{group.text.strip()}]')
# Each Run that a revision affects gets a corresponding Revision object.
# The revisions' collection is considerably larger than the condensed form we printed above,
# depending on how many Runs we have segmented the document into during Microsoft Word editing.
print(f'\n{revisions.count} revisions:')
for revision in revisions:
    # A StyleDefinitionChange strictly affects styles and not document nodes. This means the "parent_style"
    # property will always be in use, while the "parent_node" will always be None.
    # Since all other changes affect nodes, "parent_node" will conversely be in use, and "parent_style" will be None.
    if revision.revision_type == aw.RevisionType.STYLE_DEFINITION_CHANGE:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, style: [{revision.parent_style.name}]')
    else:
        print(f'\tRevision type "{revision.revision_type}", ' + f'author: {revision.author}, contents: [{revision.parent_node.get_text().strip()}]')
# Reject all revisions via the collection, reverting the document to its original form.
revisions.reject_all()
self.assertEqual(0, revisions.count)
```

### See Also

* module [aspose.words](../../)
* class [Revision](../)

