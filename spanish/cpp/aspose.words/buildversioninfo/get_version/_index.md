---
title: "Método Aspose::Words::BuildVersionInfo::get_Version"
linktitle: "get_Version"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::BuildVersionInfo::get_Version. Obtiene la versión del producto en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/buildversioninfo/get_version/
---
## BuildVersionInfo::get_Version method


Obtiene la versión del producto.

```cpp
static System::String Aspose::Words::BuildVersionInfo::get_Version()
```

## Observaciones


La versión del producto está en el formato "Major.Minor.Hotfix.0".

## Ejemplos



Muestra cómo mostrar información sobre la versión instalada de Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Ver también

* Class [BuildVersionInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
