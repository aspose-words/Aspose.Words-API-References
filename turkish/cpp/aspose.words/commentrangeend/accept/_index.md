---
title: "Aspose::Words::CommentRangeEnd::Accept yöntemi"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CommentRangeEnd::Accept yöntemi. C++'ta bir ziyaretçiyi kabul eder."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/commentrangeend/accept/
---
## CommentRangeEnd::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::CommentRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümü ziyaret edecek ziyaretçi. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Açıklamalar


[VisitCommentRangeEnd()](../../documentvisitor/visitcommentrangeend/) çağırır.

Daha fazla bilgi için Visitor tasarım desenine bakın.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../documentvisitor/)
* Class [CommentRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
