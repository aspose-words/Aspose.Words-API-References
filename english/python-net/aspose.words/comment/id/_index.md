---
title: Comment.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for Python
description: "Comment.id property. Gets or sets the comment identifier."
type: docs
weight: 60
url: /python-net/aspose.words/comment/id/
---

## Comment.id property

Gets or sets the comment identifier.


```python
@property
def id(self) -> int:
    ...

@id.setter
def id(self, value: int):
    ...

```

### Remarks

The comment identifier allows to anchor a comment to a region of text in the document.
The region must be demarcated using the [CommentRangeStart](../../commentrangestart/) and [CommentRangeEnd](../../commentrangeend/)
object sharing the same identifier value as the [Comment](../) object.

You would use this value when looking for the [CommentRangeStart](../../commentrangestart/) and
[CommentRangeEnd](../../commentrangeend/) nodes that are linked to this comment.

Comment identifiers are supposed to be unique across a document and Aspose.Words automatically 
maintains comment identifiers when loading, saving and combining documents.




### See Also

* module [aspose.words](../../)
* class [Comment](../)

