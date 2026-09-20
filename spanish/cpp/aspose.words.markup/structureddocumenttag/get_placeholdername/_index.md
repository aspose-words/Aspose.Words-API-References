---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName método"
linktitle: "get_PlaceholderName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName método. Obtiene o establece Name del BuildingBlock que contiene placeholder text en C++."
type: docs
weight: 27000
url: /es/cpp/aspose.words.markup/structureddocumenttag/get_placeholdername/
---
## StructuredDocumentTag::get_PlaceholderName method


Obtiene o establece el Nombre del [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) que contiene el texto de marcador de posición.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName() override
```


## Ejemplos



Muestra cómo usar el contenido de un bloque de construcción como texto de marcador de posición personalizado para una etiqueta de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserte una etiqueta de documento estructurado de texto sin formato del tipo "PlainText", que funcionará como un cuadro de texto.
// El contenido que mostrará por defecto es el mensaje "Haga clic aquí para introducir texto.".
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Podemos hacer que la etiqueta muestre el contenido de un bloque de construcción en lugar del texto predeterminado.
// Primero, agregue un bloque de construcción con contenido al documento de glosario.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// Luego, use la propiedad "PlaceholderName" de la etiqueta de documento estructurado para referenciar ese bloque de construcción por su nombre.
tag->set_PlaceholderName(u"Custom Placeholder");

// Si "PlaceholderName" se refiere a un bloque existente en el documento de glosario del documento principal,
// podremos verificar el bloque de construcción mediante la propiedad "Placeholder".
ASPOSE_ASSERT_EQ(substituteBlock, tag->get_Placeholder());

// Establezca la propiedad "IsShowingPlaceholderText" en "true" para tratar el
// contenido actual de la etiqueta de documento estructurado como texto de marcador de posición.
// Esto significa que al hacer clic en el cuadro de texto en Microsoft Word se resaltará inmediatamente todo el contenido de la etiqueta.
// Establezca la propiedad "IsShowingPlaceholderText" en "false" para obtener el
// etiqueta de documento estructurado para que trate su contenido como texto que ya ha introducido un usuario.
// Al hacer clic en este texto en Microsoft Word se colocará el cursor intermitente en la ubicación pulsada.
tag->set_IsShowingPlaceholderText(isShowingPlaceholderText);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## Ver también

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
