---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId método"
linktitle: "get_IgnoreDmlUniqueId"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId método. Especifica si se debe ignorar la diferencia en el ID único de DrawingML en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.comparing/advancedcompareoptions/get_ignoredmluniqueid/
---
## AdvancedCompareOptions::get_IgnoreDmlUniqueId method


Especifica si se debe ignorar la diferencia en el Id único de DrawingML.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId() const
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

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
