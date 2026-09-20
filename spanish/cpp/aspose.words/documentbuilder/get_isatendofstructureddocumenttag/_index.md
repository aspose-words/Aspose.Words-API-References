---
title: "Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag método"
linktitle: "get_IsAtEndOfStructuredDocumentTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag método. Devuelve true si el cursor está al final de una etiqueta de documento estructurado en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words/documentbuilder/get_isatendofstructureddocumenttag/
---
## DocumentBuilder::get_IsAtEndOfStructuredDocumentTag method


Devuelve **true** si el cursor está al final de una etiqueta de documento estructurado.

```cpp
bool Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag()
```


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
