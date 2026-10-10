---
title: "Aspose::Words::Comparing::CompareOptions::get_Granularity método"
linktitle: "get_Granularity"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comparing::CompareOptions::get_Granularity método. Especifica si los cambios se rastrean por carácter o por palabra en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.comparing/compareoptions/get_granularity/
---
## CompareOptions::get_Granularity method


Especifica si los cambios se rastrean por carácter o por palabra.

```cpp
Aspose::Words::Comparing::Granularity Aspose::Words::Comparing::CompareOptions::get_Granularity() const
```


## Ejemplos



Muestra cómo especificar una granularidad al comparar documentos.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Especifique si los cambios están siendo rastreados
// por carácter ('Granularity.CharLevel'), o por palabra ('Granularity.WordLevel').
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// La colección de grupos de revisiones del primer documento contiene todas las diferencias entre los documentos.
System::SharedPtr<Aspose::Words::RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## Ver también

* Enum [Granularity](../../granularity/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
