---
title: "Método Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions"
linktitle: "get_AdvancedOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions. Especifica opciones avanzadas de comparación que pueden ayudar a producir una salida de comparación más precisa en C++."
type: docs
weight: 2500
url: /es/cpp/aspose.words.comparing/compareoptions/get_advancedoptions/
---
## CompareOptions::get_AdvancedOptions method


Especifica opciones avanzadas de comparación que pueden ayudar a producir una salida de comparación más precisa.

```cpp
const System::SharedPtr<Aspose::Words::Comparing::AdvancedCompareOptions> & Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions() const
```


## Ejemplos



Muestra cómo comparar documentos ignorando el ID único de DML.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID original.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID compare.docx");

// Por defecto, Aspose.Words no ignora el ID único de DML, y el recuento de revisiones era 2.
// Si estamos ignorando el ID único de DML, el recuento de revisiones sería 0.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## Ver también

* Class [AdvancedCompareOptions](../../advancedcompareoptions/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
