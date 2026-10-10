---
title: "Aspose::Words::Paragraph::Accept metodu"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::Accept metodu. C++'ta bir ziyaretçiyi kabul eder."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/paragraph/accept/
---
## Paragraph::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::Paragraph::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümleri ziyaret edecek ziyaretçi. |

### ReturnValue

Tüm düğümler ziyaret edildiyse true; [DocumentVisitor](../../documentvisitor/) tüm düğümleri ziyaret etmeden işlemi durdurmuşsa false.
## Açıklamalar


Bu düğüm ve tüm alt düğümlerini yineleyerek dolaşır. Her düğüm, [DocumentVisitor](../../documentvisitor/) üzerindeki ilgili metodu çağırır.

Daha fazla bilgi için Visitor tasarım desenine bakın.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../documentvisitor/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
