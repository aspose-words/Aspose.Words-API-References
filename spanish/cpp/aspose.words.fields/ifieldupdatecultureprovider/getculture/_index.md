---
title: "Método Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture"
linktitle: "GetCulture"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture. Devuelve un objeto CultureInfo que se utilizará durante la actualización del campo en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider::GetCulture method


Devuelve un objeto **CultureInfo** que se utilizará durante la actualización del campo.

```cpp
virtual System::SharedPtr<System::Globalization::CultureInfo> Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture(System::String culture, System::SharedPtr<Aspose::Words::Fields::Field> field)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| cultura | System::String | El nombre de la cultura solicitada para el campo que se está actualizando. |
| campo | System::SharedPtr\<Aspose::Words::Fields::Field\> | El campo que se está actualizando. |

### ReturnValue

El objeto de cultura que debe usarse para la actualización del campo.

## Ver también

* Class [Field](../../field/)
* Interface [IFieldUpdateCultureProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
