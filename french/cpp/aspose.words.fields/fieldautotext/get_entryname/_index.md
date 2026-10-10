---
title: "Aspose::Words::Fields::FieldAutoText::get_EntryName méthode"
linktitle: "get_EntryName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldAutoText::get_EntryName méthode. Obtient ou définit le nom de l’entrée AutoText en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldautotext/get_entryname/
---
## FieldAutoText::get_EntryName method


Obtient ou définit le nom de l'entrée AutoText.

```cpp
System::String Aspose::Words::Fields::FieldAutoText::get_EntryName() override
```


## Exemples



Montre comment afficher un bloc de construction avec les champs AUTOTEXT et GLOSSARY.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez un document de glossaire et ajoutez-y un bloc de construction AutoText.
doc->set_GlossaryDocument(System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>());
auto buildingBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(doc->get_GlossaryDocument());
buildingBlock->set_Name(u"MyBlock");
buildingBlock->set_Gallery(Aspose::Words::BuildingBlocks::BuildingBlockGallery::AutoText);
buildingBlock->set_Category(u"General");
buildingBlock->set_Description(u"MyBlock description");
buildingBlock->set_Behavior(Aspose::Words::BuildingBlocks::BuildingBlockBehavior::Paragraph);
doc->get_GlossaryDocument()->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(buildingBlock);

// Créez une source et ajoutez‑la en texte à notre bloc de construction.
auto buildingBlockSource = System::MakeObject<Aspose::Words::Document>();
auto buildingBlockSourceBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(buildingBlockSource);
buildingBlockSourceBuilder->Writeln(u"Hello World!");

System::SharedPtr<Aspose::Words::Node> buildingBlockContent = doc->get_GlossaryDocument()->ImportNode(buildingBlockSource->get_FirstSection(), true);
buildingBlock->AppendChild<System::SharedPtr<Aspose::Words::Node>>(buildingBlockContent);

// Définissez un fichier contenant des parties que notre document, ou son modèle joint, peut ne pas contenir.
doc->get_FieldOptions()->set_BuiltInTemplatesPaths(System::MakeArray<System::String>({get_MyDir() + u"Busniess brochure.dotx"}));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici deux façons d'utiliser les champs pour afficher le contenu de notre bloc de construction.
// 1 -  Utilisation d'un champ AUTOTEXT :
auto fieldAutoText = System::ExplicitCast<Aspose::Words::Fields::FieldAutoText>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoText, true));
fieldAutoText->set_EntryName(u"MyBlock");

ASSERT_EQ(u" AUTOTEXT  MyBlock", fieldAutoText->GetFieldCode());

// 2 -  Utilisation d'un champ GLOSSARY :
auto fieldGlossary = System::ExplicitCast<Aspose::Words::Fields::FieldGlossary>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGlossary, true));
fieldGlossary->set_EntryName(u"MyBlock");

ASSERT_EQ(u" GLOSSARY  MyBlock", fieldGlossary->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.AUTOTEXT.GLOSSARY.dotx");
```

## Voir aussi

* Class [FieldAutoText](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
