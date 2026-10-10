---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop método"
linktitle: "get_ScaleCrop"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop método. Indica si la miniatura del documento está recortada o escalada para ajustarse a la pantalla en C++."
type: docs
weight: 24500
url: /es/cpp/aspose.words.properties/builtindocumentproperties/get_scalecrop/
---
## BuiltInDocumentProperties::get_ScaleCrop method


Indica si la miniatura del documento está recortada o escalada para ajustarse a la pantalla.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop()
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
