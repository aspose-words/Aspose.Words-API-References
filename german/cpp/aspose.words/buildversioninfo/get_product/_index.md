---
title: "Aspose::Words::BuildVersionInfo::get_Product Methode"
linktitle: "get_Product"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BuildVersionInfo::get_Product method. Gibt den vollständigen Namen des Produkts in C++ zurück."
type: docs
weight: 1000
url: /de/cpp/aspose.words/buildversioninfo/get_product/
---
## BuildVersionInfo::get_Product method


Gibt den vollständigen Namen des Produkts zurück.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Product()
```


## Beispiele



Zeigt, wie Informationen über Ihre installierte Version von Aspose.Words angezeigt werden.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Siehe auch

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
