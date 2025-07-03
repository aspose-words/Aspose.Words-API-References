---
title: Aspose::Words::CommentRangeEnd::CommentRangeEnd constructor
linktitle: CommentRangeEnd
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CommentRangeEnd::CommentRangeEnd constructor. Initializes a new instance of this class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/commentrangeend/commentrangeend/
---
## CommentRangeEnd::CommentRangeEnd constructor


Initializes a new instance of this class.

```cpp
Aspose::Words::CommentRangeEnd::CommentRangeEnd(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, int32_t id)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
| id | int32_t | The comment identifier to which this object is linked. |
## Remarks


When [CommentRangeEnd](../) is created, it belongs to the specified document, but is not yet part of the document and [ParentNode](../../node/get_parentnode/) is **null**.

To append a [CommentRangeEnd](../) to the document use InsertAfter or InsertBefore on the paragraph where you want the comment inserted.

## See Also

* Class [DocumentBase](../../documentbase/)
* Class [CommentRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
