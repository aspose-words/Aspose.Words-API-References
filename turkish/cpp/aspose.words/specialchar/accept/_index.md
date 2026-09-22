---
title: "Aspose::Words::SpecialChar::Accept yöntemi"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::SpecialChar::Accept yöntemi. C++'ta bir ziyaretçiyi kabul eder."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/specialchar/accept/
---
## SpecialChar::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::SpecialChar::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümü ziyaret edecek ziyaretçi. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Açıklamalar


Çağırır [VisitSpecialChar()](../../documentvisitor/visitspecialchar/).

Daha fazla bilgi için Visitor tasarım desenine bakın.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../documentvisitor/)
* Class [SpecialChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
