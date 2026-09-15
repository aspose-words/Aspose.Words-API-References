---
title: "طريقة Aspose::Words::BookmarkEnd::Accept"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::BookmarkEnd::Accept. تقبل زائرًا في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/bookmarkend/accept/
---
## BookmarkEnd::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::BookmarkEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقدة. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## ملاحظات


ينادي [VisitBookmarkEnd()](../../documentvisitor/visitbookmarkend/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

## انظر أيضًا

* Class [DocumentVisitor](../../documentvisitor/)
* Class [BookmarkEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
