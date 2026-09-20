---
title: "Aspose::Words::Markup::StructuredDocumentTag::Clear método"
linktitle: "Clear"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::Clear método. Borra el contenido de esta etiqueta de documento estructurado y muestra un marcador de posición si está definido en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag::Clear method


Borra el contenido de esta etiqueta de documento estructurado y muestra un marcador de posición si está definido.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::Clear()
```

## Observaciones


No es posible borrar el contenido de una etiqueta de documento estructurado si tiene revisiones.

Si esta etiqueta de documento estructurado está mapeada a XML personalizado (usando la propiedad [XmlMapping](../get_xmlmapping/)), el nodo XML referenciado se borra.

## Ejemplos



Muestra cómo eliminar el contenido de los elementos de etiqueta de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea una etiqueta de documento estructurado de texto plano y luego añádela al documento.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Esta etiqueta de documento estructurado, que tiene forma de cuadro de texto, ya muestra texto de marcador de posición.
ASSERT_EQ(u"Click here to enter text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Crea un bloque de construcción con contenido de texto.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();
auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"My placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->EnsureMinimum();
substituteBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(glossaryDoc, u"Custom placeholder text."));
glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Establece la propiedad "PlaceholderName" de la etiqueta de documento estructurado al nombre de nuestro bloque de construcción para obtener
// que la etiqueta de documento estructurado muestre el contenido del bloque de construcción en lugar del texto predeterminado original.
tag->set_PlaceholderName(u"My placeholder");

ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// Edita el texto de la etiqueta de documento estructurado y oculta el texto del marcador de posición.
auto run = System::ExplicitCast<Aspose::Words::Run>(tag->GetChild(Aspose::Words::NodeType::Run, 0, true));
run->set_Text(u"New text.");
tag->set_IsShowingPlaceholderText(false);

ASSERT_EQ(u"New text.", tag->GetText().Trim());

// Utiliza el método "Clear" para borrar el contenido de esta etiqueta de documento estructurado y mostrar nuevamente el marcador de posición.
tag->Clear();

ASSERT_TRUE(tag->get_IsShowingPlaceholderText());
ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
```

## Ver también

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
