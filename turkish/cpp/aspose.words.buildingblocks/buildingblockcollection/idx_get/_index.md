---
title: "Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get yöntemi. C++'ta verilen indeksteki bir yapı bloğunu alır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.buildingblocks/buildingblockcollection/idx_get/
---
## BuildingBlockCollection::idx_get method


Belirtilen indeksteki bir yapı taşını alır.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::BuildingBlockCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Yapı blokları listesindeki bir indeks. |
## Açıklamalar


İndeks sıfır tabanlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

İndeks listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

İndeks negatif ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

## Ayrıca Bakınız

* Class [BuildingBlock](../../buildingblock/)
* Class [BuildingBlockCollection](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
