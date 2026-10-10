---
title: "Clase Aspose::Words::Range"
linktitle: "Rango"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Range. Representa un área contigua en un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 51000
url: /es/cpp/aspose.words/range/
---
## Range class


Representa un área contigua en un documento. Para obtener más información, visite el artículo de documentación [Working with Ranges](https://docs.aspose.com/words/cpp/working-with-ranges/).

```cpp
class Range : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Delete](./delete/)() | Elimina todos los caracteres del rango. |
| [get_Bookmarks](./get_bookmarks/)() | Devuelve una colección de [Bookmarks](./get_bookmarks/) que representa todos los marcadores en el rango. |
| [get_Fields](./get_fields/)() | Devuelve una colección de [Fields](./get_fields/) que representa todos los campos en el rango. |
| [get_FormFields](./get_formfields/)() | Devuelve una colección de [FormFields](./get_formfields/) que representa todos los campos de formulario en el rango. |
| [get_Revisions](./get_revisions/)() | Obtiene una colección de revisiones (cambios controlados) que existen en este rango. |
| [get_StructuredDocumentTags](./get_structureddocumenttags/)() | Devuelve una colección de [StructuredDocumentTags](./get_structureddocumenttags/) que representa todas las etiquetas estructuradas del documento en el rango. |
| [get_Text](./get_text/)() | Obtiene el texto del rango. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Cambia los valores del tipo de campo [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) de [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/) y [FieldEnd](../../aspose.words.fields/fieldend/) en este rango para que correspondan a los tipos de campo contenidos en los códigos de campo. |
| [Replace](./replace/)(const System::String\&, const System::String\&) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Reemplaza todas las apariciones de un patrón de caracteres especificado por una expresión regular con otra cadena. |
| [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Reemplaza todas las apariciones de un patrón de caracteres especificado por una expresión regular con otra cadena. |
| [ToDocument](./todocument/)() | Construye un nuevo documento completamente formado que contiene el rango. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Desvincula los campos en este rango. |
| [UpdateFields](./updatefields/)() | Actualiza los valores de los campos del documento en este rango. |
## Observaciones


El documento se representa mediante un árbol de nodos y los nodos proporcionan operaciones para trabajar con el árbol, pero algunas operaciones son más fáciles de realizar si el documento se trata como una secuencia contigua de texto.

[Range](./) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## Ejemplos



Muestra cómo obtener el contenido de texto de todos los nodos que cubre un rango.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
