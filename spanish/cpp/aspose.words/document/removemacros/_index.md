---
title: "Método Aspose::Words::Document::RemoveMacros"
linktitle: "RemoveMacros"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::RemoveMacros. Elimina todas las macros (el proyecto VBA) así como barras de herramientas y personalizaciones de comandos del documento en C++."
type: docs
weight: 69000
url: /es/cpp/aspose.words/document/removemacros/
---
## Document::RemoveMacros method


Elimina todas las macros (el proyecto VBA) así como las barras de herramientas y las personalizaciones de comandos del documento.

```cpp
void Aspose::Words::Document::RemoveMacros()
```

## Observaciones


Al eliminar todas las macros de un documento, puedes asegurarte de que el documento no contenga virus de macros.

## Ejemplos



Muestra cómo eliminar todas las macros de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");

ASSERT_TRUE(doc->get_HasMacros());
ASSERT_EQ(u"Project", doc->get_VbaProject()->get_Name());

// Elimina el proyecto VBA del documento, junto con todas sus macros.
doc->RemoveMacros();

ASSERT_FALSE(doc->get_HasMacros());
ASSERT_TRUE(System::TestTools::IsNull(doc->get_VbaProject()));
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
