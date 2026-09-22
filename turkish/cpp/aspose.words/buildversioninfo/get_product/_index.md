---
title: "Aspose::Words::BuildVersionInfo::get_Product yöntemi"
linktitle: "get_Product"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BuildVersionInfo::get_Product yöntemi. C++'ta ürünün tam adını alır."
type: docs
weight: 1000
url: /tr/cpp/aspose.words/buildversioninfo/get_product/
---
## BuildVersionInfo::get_Product method


Ürünün tam adını alır.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Product()
```


## Örnekler



Yüklü Aspose.Words sürümünüz hakkında bilgiyi nasıl görüntüleyeceğinizi gösterir.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Ayrıca Bakınız

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
