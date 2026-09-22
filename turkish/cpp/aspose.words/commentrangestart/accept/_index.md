---
title: "Aspose::Words::CommentRangeStart::Accept method"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CommentRangeStart::Accept method. C++'ta bir ziyaretçi kabul eder."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/commentrangestart/accept/
---
## CommentRangeStart::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::CommentRangeStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümü ziyaret edecek ziyaretçi. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Açıklamalar


[VisitCommentRangeStart()](../../documentvisitor/visitcommentrangestart/) çağırır.

Daha fazla bilgi için Visitor tasarım desenine bakın.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../documentvisitor/)
* Class [CommentRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
