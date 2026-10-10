---
title: "Aspose::Words::BuildVersionInfo::get_Product metod"
linktitle: "get_Product"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BuildVersionInfo::get_Product metod. Hämtar produktens fullständiga namn i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words/buildversioninfo/get_product/
---
## BuildVersionInfo::get_Product method


Hämtar produktens fullständiga namn.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Product()
```


## Exempel



Visar hur man visar information om din installerade version av Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Se även

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
