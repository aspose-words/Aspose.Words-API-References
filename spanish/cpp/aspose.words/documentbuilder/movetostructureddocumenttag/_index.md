---
title: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag método"
linktitle: "MoveToStructuredDocumentTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag método. Mueve el cursor a la etiqueta de documento estructurado en C++."
type: docs
weight: 61000
url: /es/cpp/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) method


Mueve el cursor a la etiqueta de documento estructurado.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> &structuredDocumentTag, int32_t characterIndex)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| structuredDocumentTag | const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\& | La etiqueta de documento estructurado a la que moverse. |
| characterIndex | int32_t | El índice del carácter dentro de la etiqueta de documento estructurado. Un valor negativo permite especificar una posición desde el final de la etiqueta de documento estructurado. Usa -1 para mover al final de la etiqueta de documento estructurado. Si la etiqueta de documento estructurado está a nivel de bloque y deseas mover el cursor al final de su último párrafo, especifica -2. |

## Ejemplos



Muestra cómo mover el cursor de [DocumentBuilder](../) dentro de una etiqueta de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Hay varias formas de mover el cursor:
// 1 -  Mover al primer carácter de la etiqueta de documento estructurado por índice.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Mover al primer carácter de la etiqueta de documento estructurado por objeto.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Mover al final de la segunda etiqueta de documento estructurado.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Obtener la etiqueta de documento estructurado seleccionada actualmente.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## Ver también

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToStructuredDocumentTag(int32_t, int32_t) method


Mueve el cursor a una etiqueta de documento estructurado en la sección actual.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(int32_t structuredDocumentTagIndex, int32_t characterIndex)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| structuredDocumentTagIndex | int32_t | El índice de la etiqueta de documento estructurado a la que mover. |
| characterIndex | int32_t | El índice del carácter dentro de la etiqueta de documento estructurado. Un valor negativo permite especificar una posición desde el final de la etiqueta de documento estructurado. Usa -1 para mover al final de la etiqueta de documento estructurado. Si la etiqueta de documento estructurado está a nivel de bloque y deseas mover el cursor al final de su último párrafo, especifica -2. |
## Observaciones


La navegación se realiza dentro de la historia actual de la sección actual. Es decir, si moviste el cursor al encabezado principal de la primera sección, entonces *structuredDocumentTagIndex* especifica el índice de la etiqueta de documento estructurado dentro de ese encabezado de esa sección.

Cuando *structuredDocumentTagIndex* es mayor o igual que 0, especifica un índice desde el comienzo de la sección, siendo 0 la primera etiqueta de documento estructurado. Cuando *structuredDocumentTagIndex* es menor que 0, especifica un índice desde el final de la sección, siendo -1 la última etiqueta de documento estructurado.

## Ejemplos



Muestra cómo mover el cursor de [DocumentBuilder](../) dentro de una etiqueta de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Hay varias formas de mover el cursor:
// 1 -  Mover al primer carácter de la etiqueta de documento estructurado por índice.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Mover al primer carácter de la etiqueta de documento estructurado por objeto.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Mover al final de la segunda etiqueta de documento estructurado.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Obtener la etiqueta de documento estructurado seleccionada actualmente.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
