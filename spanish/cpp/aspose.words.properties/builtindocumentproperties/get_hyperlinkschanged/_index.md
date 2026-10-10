---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged método"
linktitle: "get_HyperlinksChanged"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged método. Indica si los hipervínculos en un documento fueron modificados en C++."
type: docs
weight: 13500
url: /es/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkschanged/
---
## BuiltInDocumentProperties::get_HyperlinksChanged method


Indica si los hipervínculos en un documento fueron modificados.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged()
```

## Observaciones


Aspose.Words no actualiza esta propiedad.

## Ejemplos



Muestra cómo obtener propiedades extendidas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## Ver también

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
