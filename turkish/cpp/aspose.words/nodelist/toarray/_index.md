---
title: "Aspose::Words::NodeList::ToArray yöntemi"
linktitle: "ToArray"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeList::ToArray yöntemi. C++'ta koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/nodelist/toarray/
---
## NodeList::ToArray method


Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeList::ToArray() const
```


### ReturnValue

Düğümlerden oluşan bir dizi.
## Açıklamalar


Bir düğüm koleksiyonunu iterasyon sırasında düğüm eklememeli/kaldırmamalısınız çünkü bu, yineleyiciyi geçersiz kılar ve canlı koleksiyonlar için yenileme gerektirir.

İterasyon sırasında düğüm ekleyip/çıkarmak için, düğümleri sabit boyutlu bir diziye kopyalamak ve ardından dizi üzerinde iterasyon yapmak amacıyla bu yöntemi kullanın.

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
