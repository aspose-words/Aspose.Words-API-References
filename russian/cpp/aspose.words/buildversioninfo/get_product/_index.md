---
title: "Метод Aspose::Words::BuildVersionInfo::get_Product"
linktitle: "get_Product"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::BuildVersionInfo::get_Product. Возвращает полное название продукта в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words/buildversioninfo/get_product/
---
## BuildVersionInfo::get_Product method


Возвращает полное название продукта.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Product()
```


## Примеры



Показывает, как отобразить информацию о установленной версии Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## См. также

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
