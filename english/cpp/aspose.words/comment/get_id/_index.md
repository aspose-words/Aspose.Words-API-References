---
title: Aspose::Words::Comment::get_Id method
linktitle: get_Id
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comment::get_Id method. Gets or sets the comment identifier in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words/comment/get_id/
---
## Comment::get_Id method


Gets or sets the comment identifier.

```cpp
int32_t Aspose::Words::Comment::get_Id() const
```

## Remarks


The comment identifier allows to anchor a comment to a region of text in the document. The region must be demarcated using the [CommentRangeStart](../../commentrangestart/) and [CommentRangeEnd](../../commentrangeend/) object sharing the same identifier value as the [Comment](../) object.

You would use this value when looking for the [CommentRangeStart](../../commentrangestart/) and [CommentRangeEnd](../../commentrangeend/) nodes that are linked to this comment.

[Comment](../) identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents. 
## See Also

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
