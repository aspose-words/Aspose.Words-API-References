---
title: "Aspose::Words::BuildVersionInfo::get_Product método"
linktitle: "get_Product"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BuildVersionInfo::get_Product método. Obtiene el nombre completo del producto en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words/buildversioninfo/get_product/
---
## BuildVersionInfo::get_Product method


Obtiene el nombre completo del producto.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Product()
```


## Ejemplos



Muestra cómo mostrar información sobre la versión instalada de Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Ver también

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
