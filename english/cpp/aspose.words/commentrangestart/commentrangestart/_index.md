---
title: Aspose::Words::CommentRangeStart::CommentRangeStart constructor
linktitle: CommentRangeStart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CommentRangeStart::CommentRangeStart constructor. Initializes a new instance of this class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/commentrangestart/commentrangestart/
---
## CommentRangeStart::CommentRangeStart constructor


Initializes a new instance of this class.

```cpp
Aspose::Words::CommentRangeStart::CommentRangeStart(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, int32_t id)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
| id | int32_t | The comment identifier to which this object is linked. |
## Remarks


When [CommentRangeStart](../) is created, it belongs to the specified document, but is not yet part of the document and [ParentNode](../../node/get_parentnode/) is **null**.

To append a [CommentRangeStart](../) to the document use InsertAfter or InsertBefore on the paragraph where you want the comment inserted.

## See Also

* Class [DocumentBase](../../documentbase/)
* Class [CommentRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
