---
title: "Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd metodu"
linktitle: "VisitBuildingBlockEnd"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd metodu. C++'de bir building block'un numaralandırması sona erdiğinde çağrılır."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/documentvisitor/visitbuildingblockend/
---
## DocumentVisitor::VisitBuildingBlockEnd method


Bir yapı bloğunun sayımı bittiğinde çağrılır.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| blok | System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\> | Ziyaret edilen nesne. |

### ReturnValue

Sıralamayı nasıl devam ettireceğini belirten bir [VisitorAction](../../visitoraction/) değeri.
## Açıklamalar


Not: Bir building block düğümü ve alt öğeleri, bir Visitor'ı bir [Document](../../document/) üzerinde çalıştırdığınızda ziyaret edilmez. Bir building block üzerinde Visitor çalıştırmak istiyorsanız, Visitor'ı bir [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) üzerinde çalıştırmanız veya [Accept()](../../../aspose.words.buildingblocks/buildingblock/accept/) çağırmanız gerekir.

## Ayrıca Bakınız

* Enum [VisitorAction](../../visitoraction/)
* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
