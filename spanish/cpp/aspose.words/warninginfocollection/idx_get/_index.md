---
title: "Aspose::Words::WarningInfoCollection::idx_get método"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::WarningInfoCollection::idx_get método. Obtiene un elemento en el índice especificado en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words/warninginfocollection/idx_get/
---
## WarningInfoCollection::idx_get method


Obtiene un elemento en el índice especificado.

```cpp
System::SharedPtr<Aspose::Words::WarningInfo> Aspose::Words::WarningInfoCollection::idx_get(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | Índice basado en cero del elemento. |

## Ejemplos



Muestra cómo obtener advertencias sobre formatos no compatibles.
```cpp
auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_WarningCallback(warnings);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"FB2 document.fb2", loadOptions);

ASSERT_EQ(u"The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings->idx_get(0)->get_Description());
ASSERT_EQ(1, warnings->get_Count());
```

## Ver también

* Class [WarningInfo](../../warninginfo/)
* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
