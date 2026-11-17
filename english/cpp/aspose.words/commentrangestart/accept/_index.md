---
title: Aspose::Words::CommentRangeStart::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CommentRangeStart::Accept method. Accepts a visitor in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/commentrangestart/accept/
---
## CommentRangeStart::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::CommentRangeStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the node. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Remarks


Calls [VisitCommentRangeStart()](../../documentvisitor/visitcommentrangestart/).

For more info see the Visitor design pattern.

## See Also

* Class [DocumentVisitor](../../documentvisitor/)
* Class [CommentRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
