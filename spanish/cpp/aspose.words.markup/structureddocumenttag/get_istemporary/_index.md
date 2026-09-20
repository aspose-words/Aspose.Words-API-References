---
title: "Método Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary"
linktitle: "get_IsTemporary"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary. Especifica si este SDT debe eliminarse del documento WordProcessingML cuando su contenido se modifica en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.markup/structureddocumenttag/get_istemporary/
---
## StructuredDocumentTag::get_IsTemporary method


Especifica si este **SDT** debe eliminarse del documento WordProcessingML cuando su contenido se modifica.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary() const
```


## Ejemplos



Muestra cómo crear controles de un solo uso.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserte una etiqueta de documento estructurado de texto plano,
// que actuará como un formulario de texto plano en el que el usuario puede ingresar texto.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Establezca la propiedad "IsTemporary" a "true" para hacer que la etiqueta de documento estructurado desaparezca y
// asimile su contenido al documento después de que el usuario lo edite una vez en Microsoft Word.
// Establezca la propiedad "IsTemporary" a "false" para permitir al usuario editar el contenido
// de la etiqueta de documento estructurado cualquier número de veces.
tag->set_IsTemporary(isTemporary);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Please enter text: ");
builder->InsertNode(tag);

// Inserte otra etiqueta de documento estructurado en forma de casilla de verificación y establezca su estado predeterminado a "checked".
tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
tag->set_Checked(true);

// Establezca la propiedad "IsTemporary" a "true" para que la casilla de verificación se convierta en un símbolo
// una vez que el usuario haga clic en ella en Microsoft Word.
// Establezca la propiedad "IsTemporary" a "false" para permitir al usuario hacer clic en la casilla de verificación cualquier número de veces.
tag->set_IsTemporary(isTemporary);

builder->Write(u"\nPlease click the check box: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IsTemporary.docx");
```

## Ver también

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
