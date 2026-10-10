---
title: "Aspose::Words::WarningInfoCollection::get_Count método"
linktitle: "get_Count"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::WarningInfoCollection::get_Count método. Obtiene el número de elementos contenidos en la colección en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/warninginfocollection/get_count/
---
## WarningInfoCollection::get_Count method


Obtiene el número de elementos contenidos en la colección.

```cpp
int32_t Aspose::Words::WarningInfoCollection::get_Count()
```


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

* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
