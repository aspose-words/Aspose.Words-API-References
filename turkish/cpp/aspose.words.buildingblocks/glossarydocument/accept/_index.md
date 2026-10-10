---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept yöntemi"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept yöntemi. C++'ta bir ziyaretçiyi kabul eder."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.buildingblocks/glossarydocument/accept/
---
## GlossaryDocument::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::BuildingBlocks::GlossaryDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümleri ziyaret edecek ziyaretçi. |

### ReturnValue

Tüm düğümler ziyaret edildiyse true; tüm düğümler ziyaret edilmeden önce [DocumentVisitor](../../../aspose.words/documentvisitor/) işlemi durdurduysa false.
## Açıklamalar


Bu düğüm ve tüm alt düğümlerini yineleyerek dolaşır. Her düğüm, [DocumentVisitor](../../../aspose.words/documentvisitor/) üzerindeki ilgili yöntemi çağırır.

Daha fazla bilgi için Visitor tasarım desenine bakın.

Önce [VisitGlossaryDocumentStart()](../../../aspose.words/documentvisitor/visitglossarydocumentstart/) çağırır, ardından bu düğümün tüm alt düğümleri için [Accept()](../../../aspose.words/node/accept/) çağırır ve sonunda [VisitGlossaryDocumentEnd()](../../../aspose.words/documentvisitor/visitglossarydocumentend/) çağırır.

Not: Bir sözlük belge düğümü ve alt düğümleri, bir [Document](../../../aspose.words/document/) üzerinde Ziyaretçi (Visitor) çalıştırdığınızda ziyaret edilmez. Bir sözlük belgesi üzerinde Ziyaretçi çalıştırmak istiyorsanız, [Accept()](./) çağırmanız gerekir.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
