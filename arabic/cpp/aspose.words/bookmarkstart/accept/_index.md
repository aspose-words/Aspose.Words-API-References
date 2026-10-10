---
title: "Aspose::Words::BookmarkStart::Accept طريقة"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BookmarkStart::Accept طريقة. يقبل زائرًا في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/bookmarkstart/accept/
---
## BookmarkStart::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::BookmarkStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقدة. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## ملاحظات


يستدعي [VisitBookmarkStart()](../../documentvisitor/visitbookmarkstart/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

## انظر أيضًا

* Class [DocumentVisitor](../../documentvisitor/)
* Class [BookmarkStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
