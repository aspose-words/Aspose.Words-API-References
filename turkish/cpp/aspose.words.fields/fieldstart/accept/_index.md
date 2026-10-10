---
title: "Aspose::Words::Fields::FieldStart::Accept yöntemi"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldStart::Accept yöntemi. C++'ta bir ziyaretçiyi kabul eder."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldstart/accept/
---
## FieldStart::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::Fields::FieldStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümü ziyaret edecek ziyaretçi. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Açıklamalar


[VisitFieldStart()](../../../aspose.words/documentvisitor/visitfieldstart/) çağırır.

Daha fazla bilgi için Visitor tasarım desenine bakın.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
