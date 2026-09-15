---
title: "Aspose::Words::CommentRangeStart::Accept method"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::CommentRangeStart::Accept method. تقبل زائرًا في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/commentrangestart/accept/
---
## CommentRangeStart::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::CommentRangeStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقدة. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## ملاحظات


ينادي [VisitCommentRangeStart()](../../documentvisitor/visitcommentrangestart/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

## انظر أيضًا

* Class [DocumentVisitor](../../documentvisitor/)
* Class [CommentRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
