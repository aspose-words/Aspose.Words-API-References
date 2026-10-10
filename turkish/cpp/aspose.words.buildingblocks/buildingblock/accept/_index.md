---
title: "Aspose::Words::BuildingBlocks::BuildingBlock::Accept yöntemi"
linktitle: "Accept"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BuildingBlocks::BuildingBlock::Accept yöntemi. C++'ta bir ziyaretçiyi kabul eder."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock::Accept method


Bir ziyaretçiyi kabul eder.

```cpp
bool Aspose::Words::BuildingBlocks::BuildingBlock::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ziyaretçi | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Düğümleri ziyaret edecek ziyaretçi. |

### ReturnValue

Tüm düğümler ziyaret edildiyse true; tüm düğümler ziyaret edilmeden önce [DocumentVisitor](../../../aspose.words/documentvisitor/) işlemi durdurduysa false.
## Açıklamalar


Bu düğüm ve tüm alt düğümlerini yineleyerek dolaşır. Her düğüm, [DocumentVisitor](../../../aspose.words/documentvisitor/) üzerindeki ilgili yöntemi çağırır.

Daha fazla bilgi için Visitor tasarım desenine bakın.

[VisitBuildingBlockStart()](../../../aspose.words/documentvisitor/visitbuildingblockstart/) çağırır, ardından bu building block'un tüm alt düğümleri için [Accept()](../../../aspose.words/node/accept/) çağırır, ardından [VisitBuildingBlockEnd()](../../../aspose.words/documentvisitor/visitbuildingblockend/) çağırır.

Not: Bir building block düğümü ve alt öğeleri, bir [Document](../../../aspose.words/document/) üzerinde Visitor çalıştırdığınızda ziyaret edilmez. Bir building block üzerinde Visitor çalıştırmak istiyorsanız, ziyaretçiyi [GlossaryDocument](../../glossarydocument/) üzerinde çalıştırmalı veya [Accept()](./) çağırmalısınız.

## Ayrıca Bakınız

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
