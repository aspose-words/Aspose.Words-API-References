---
title: "Метод Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart"
linktitle: "VisitGlossaryDocumentStart"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart. Вызывается, когда началось перечисление глоссарного документа в C++."
type: docs
weight: 28000
url: /ru/cpp/aspose.words/documentvisitor/visitglossarydocumentstart/
---
## DocumentVisitor::VisitGlossaryDocumentStart method


Вызывается, когда начинается перечисление глоссарного документа.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
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
