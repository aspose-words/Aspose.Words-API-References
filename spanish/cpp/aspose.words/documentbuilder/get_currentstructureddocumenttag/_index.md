---
title: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag método"
linktitle: "get_CurrentStructuredDocumentTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag método. Obtiene la etiqueta de documento estructurado que está actualmente seleccionada en este DocumentBuilder en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words/documentbuilder/get_currentstructureddocumenttag/
---
## DocumentBuilder::get_CurrentStructuredDocumentTag method


Obtiene la etiqueta de documento estructurado que está actualmente seleccionada en este [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::get_CurrentStructuredDocumentTag()
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

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
