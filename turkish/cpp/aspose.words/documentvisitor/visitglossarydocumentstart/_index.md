---
title: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart yöntemi"
linktitle: "VisitGlossaryDocumentStart"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart yöntemi. C++'ta bir sözlük belgesinin sayımı başladığında çağrılır."
type: docs
weight: 28000
url: /tr/cpp/aspose.words/documentvisitor/visitglossarydocumentstart/
---
## DocumentVisitor::VisitGlossaryDocumentStart method


Sözlük belgesinin numaralandırması başladığında çağrılır.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| glossary | System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> | Ziyaret edilen nesne. |

### ReturnValue

Sıralamayı nasıl devam ettireceğini belirten bir [VisitorAction](../../visitoraction/) değeri.
## Açıklamalar


Not: Bir sözlük belge düğümü ve alt öğeleri, bir [Document](../../document/) üzerinde bir Visitor çalıştırdığınızda ziyaret edilmez. Bir sözlük belgesi üzerinde bir Visitor çalıştırmak istiyorsanız, [Accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/) metodunu çağırmanız gerekir.

## Ayrıca Bakınız

* Enum [VisitorAction](../../visitoraction/)
* Class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
