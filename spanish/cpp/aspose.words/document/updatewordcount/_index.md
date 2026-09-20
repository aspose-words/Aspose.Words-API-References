---
title: "Método Aspose::Words::Document::UpdateWordCount"
linktitle: "UpdateWordCount"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::UpdateWordCount. Actualiza las propiedades de recuento de palabras del documento en C++."
type: docs
weight: 101000
url: /es/cpp/aspose.words/document/updatewordcount/
---
## Document::UpdateWordCount() method


Actualiza las propiedades de recuento de palabras del documento.

```cpp
void Aspose::Words::Document::UpdateWordCount()
```

## Observaciones


[UpdateWordCount](./) recalculates and updates Characters, [Words](../../) and Paragraphs properties in the [BuiltInDocumentProperties](../get_builtindocumentproperties/) collection of the [Document](../).

Tenga en cuenta que [UpdateWordCount](./) no actualiza las propiedades de número de líneas y páginas. Use la sobrecarga de [UpdateWordCount](./) y pase el valor **true** como parámetro para hacerlo.

Cuando utiliza una versión de evaluación, la marca de agua de evaluación también se incluirá en el recuento de palabras.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateWordCount(bool) method


Actualiza las propiedades de recuento de palabras del documento, opcionalmente actualiza la propiedad [Lines](../../../aspose.words.properties/builtindocumentproperties/get_lines/).

```cpp
void Aspose::Words::Document::UpdateWordCount(bool updateLinesCount)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| updateLinesCount | bool | **true** si se debe calcular el número de líneas en el documento. |

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
