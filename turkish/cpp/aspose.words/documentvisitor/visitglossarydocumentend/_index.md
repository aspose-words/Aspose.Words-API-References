---
title: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd metodu"
linktitle: "VisitGlossaryDocumentEnd"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd metodu. C++'de bir sözlük belgesinin numaralandırması sona erdiğinde çağrılır."
type: docs
weight: 27000
url: /tr/cpp/aspose.words/documentvisitor/visitglossarydocumentend/
---
## DocumentVisitor::VisitGlossaryDocumentEnd method


Sözlük belgesinin numaralandırması bittiğinde çağrılır.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
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
