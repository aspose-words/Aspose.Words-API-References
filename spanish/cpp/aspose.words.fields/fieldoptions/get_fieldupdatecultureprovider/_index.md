---
title: "Método Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider"
linktitle: "get_FieldUpdateCultureProvider"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider. Obtiene o establece un proveedor que devuelve un objeto de cultura específico para cada campo particular en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.fields/fieldoptions/get_fieldupdatecultureprovider/
---
## FieldOptions::get_FieldUpdateCultureProvider method


Obtiene o establece un proveedor que devuelve un objeto de cultura específico para cada campo en particular.

```cpp
const System::SharedPtr<Aspose::Words::Fields::IFieldUpdateCultureProvider> & Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider() const
```

## Observaciones


El proveedor se solicita cuando el valor de [FieldUpdateCultureSource](../get_fieldupdateculturesource/) es [FieldCode](../../fieldupdateculturesource/).

Si el proveedor está presente, el objeto de cultura que devuelve se utiliza para la actualización del campo. De lo contrario, se usa una cultura del sistema.
## Ver también

* Interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
