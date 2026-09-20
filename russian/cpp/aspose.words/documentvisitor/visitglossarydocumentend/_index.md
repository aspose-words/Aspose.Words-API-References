---
title: "Метод Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd"
linktitle: "VisitGlossaryDocumentEnd"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd. Вызывается, когда перечисление глоссарного документа завершилось в C++."
type: docs
weight: 27000
url: /ru/cpp/aspose.words/documentvisitor/visitglossarydocumentend/
---
## DocumentVisitor::VisitGlossaryDocumentEnd method


Вызывается, когда перечисление глоссарного документа завершилось.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| glossary | System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> | Объект, который посещается. |

### ReturnValue

Значение [VisitorAction](../../visitoraction/), которое указывает, как продолжить перечисление.
## Примечания


Примечание: Узел глоссарного документа и его дочерние элементы не посещаются, когда вы выполняете Visitor над [Document](../../document/). Если вы хотите выполнить Visitor над глоссарным документом, вам необходимо вызвать [Accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/).

## См. также

* Enum [VisitorAction](../../visitoraction/)
* Class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
