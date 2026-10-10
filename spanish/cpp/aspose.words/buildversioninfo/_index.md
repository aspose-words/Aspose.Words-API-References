---
title: "Aspose::Words::BuildVersionInfo class"
linktitle: "BuildVersionInfo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BuildVersionInfo class. Proporciona información sobre el nombre y la versión del producto actual. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/buildversioninfo/
---
## BuildVersionInfo class


Proporciona información sobre el nombre y la versión del producto actual. Para obtener más información, visite el artículo de documentación [Generator or Producer Name Included in Output Documents](https://docs.aspose.com/words/cpp/generator-or-producer-name-included-in-output-documents/).

```cpp
class BuildVersionInfo
```

## Métodos

| Método | Descripción |
| --- | --- |
| [BuildVersionInfo](./buildversioninfo/)() |  |
| static [get_Product](./get_product/)() | Obtiene el nombre completo del producto. |
| static [get_Version](./get_version/)() | Obtiene la versión del producto. |

## Ejemplos



Muestra cómo mostrar información sobre la versión instalada de Aspose.Words.
```cpp
std::cout << System::String::Format(u"I am currently using {0}, version number {1}!", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) << std::endl;
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
