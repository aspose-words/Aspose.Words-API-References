---
title: "Aspose::Words::NodeList::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeList::idx_get yöntemi. C++'ta verilen indeksteki bir düğümü alır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/nodelist/idx_get/
---
## NodeList::idx_get method


Verilen indeksteki bir düğümü alır.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeList::idx_get(int32_t index) const
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Düğümlerin listesine bir indeks. |
## Açıklamalar


İndeks sıfır tabanlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

İndeks listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

İndeks negatif ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
