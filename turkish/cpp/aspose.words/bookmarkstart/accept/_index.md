---
title: "Aspose::Words::BookmarkStart::Accept yöntemi"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BookmarkStart::Accept yöntemi. C++'da bir ziyaretçiyi kabul eder."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/bookmarkstart/accept/
---
## BookmarkStart::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::BookmarkStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümü ziyaret edecek ziyaretçi. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Açıklamalar


Çağırır [VisitBookmarkStart()](../../documentvisitor/visitbookmarkstart/).

Daha fazla bilgi için Visitor tasarım desenine bakın.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../documentvisitor/)
* Class [BookmarkStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
