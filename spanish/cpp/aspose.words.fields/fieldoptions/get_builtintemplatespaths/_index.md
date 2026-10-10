---
title: "Método Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths"
linktitle: "get_BuiltInTemplatesPaths"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths. Obtiene o establece las rutas de las plantillas integradas de MS Word en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fields/fieldoptions/get_builtintemplatespaths/
---
## FieldOptions::get_BuiltInTemplatesPaths method


Obtiene o establece las rutas de las plantillas integradas de MS Word.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths() const
```

## Observaciones


Esta propiedad es utilizada por los campos [FieldAutoText](../../fieldautotext/) y [FieldGlossary](../../fieldglossary/), si la entrada de texto automático referenciada no se encuentra en la plantilla [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/).

De forma predeterminada, MS Word almacena las plantillas integradas en c:\Users\<username>\AppData\Roaming\**Microsoft**\[Document](../../../aspose.words/document/) Building Blocks\1033\16\Built-In Building Blocks.dotx y en los archivos C:\Users\<username>\AppData\Roaming\**Microsoft**\Templates\Normal.dotm.

## Ejemplos



Muestra cómo mostrar un bloque de construcción con los campos AUTOTEXT y GLOSSARY.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Cree un documento de glosario y añada un bloque de construcción AutoText a él.
doc->set_GlossaryDocument(System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>());
auto buildingBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(doc->get_GlossaryDocument());
buildingBlock->set_Name(u"MyBlock");
buildingBlock->set_Gallery(Aspose::Words::BuildingBlocks::BuildingBlockGallery::AutoText);
buildingBlock->set_Category(u"General");
buildingBlock->set_Description(u"MyBlock description");
buildingBlock->set_Behavior(Aspose::Words::BuildingBlocks::BuildingBlockBehavior::Paragraph);
doc->get_GlossaryDocument()->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(buildingBlock);

// Cree una fuente y añádala como texto a nuestro bloque de construcción.
auto buildingBlockSource = System::MakeObject<Aspose::Words::Document>();
auto buildingBlockSourceBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(buildingBlockSource);
buildingBlockSourceBuilder->Writeln(u"Hello World!");

System::SharedPtr<Aspose::Words::Node> buildingBlockContent = doc->get_GlossaryDocument()->ImportNode(buildingBlockSource->get_FirstSection(), true);
buildingBlock->AppendChild<System::SharedPtr<Aspose::Words::Node>>(buildingBlockContent);

// Establezca un archivo que contenga partes que nuestro documento, o su plantilla adjunta, pueden no contener.
doc->get_FieldOptions()->set_BuiltInTemplatesPaths(System::MakeArray<System::String>({get_MyDir() + u"Busniess brochure.dotx"}));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos formas de usar campos para mostrar el contenido de nuestro bloque de construcción.
// 1 -  Usando un campo AUTOTEXT:
auto fieldAutoText = System::ExplicitCast<Aspose::Words::Fields::FieldAutoText>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoText, true));
fieldAutoText->set_EntryName(u"MyBlock");

ASSERT_EQ(u" AUTOTEXT  MyBlock", fieldAutoText->GetFieldCode());

// 2 -  Usando un campo GLOSSARY:
auto fieldGlossary = System::ExplicitCast<Aspose::Words::Fields::FieldGlossary>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGlossary, true));
fieldGlossary->set_EntryName(u"MyBlock");

ASSERT_EQ(u" GLOSSARY  MyBlock", fieldGlossary->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.AUTOTEXT.GLOSSARY.dotx");
```

## Ver también

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
