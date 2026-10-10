---
title: "Método Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters"
linktitle: "get_Characters"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters. Representa una estimación del número de caracteres en el documento en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.properties/builtindocumentproperties/get_characters/
---
## BuiltInDocumentProperties::get_Characters method


Representa una estimación del número de caracteres en el documento.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters()
```

## Observaciones


Aspose.Words actualiza esta propiedad cuando llama a [UpdateWordCount](../../../aspose.words/document/updatewordcount/).

## Ejemplos



Muestra cómo actualizar todas las etiquetas de lista en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words no rastrea métricas de documentos como estas en tiempo real.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// Para obtener valores precisos de tres de estas propiedades, necesitaremos actualizarlas manualmente.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// Para el recuento de líneas, necesitaremos llamar a una sobrecarga específica del método de actualización.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## Ver también

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
