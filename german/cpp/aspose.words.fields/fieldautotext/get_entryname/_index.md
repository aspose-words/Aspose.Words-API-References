---
title: "Aspose::Words::Fields::FieldAutoText::get_EntryName Methode"
linktitle: "get_EntryName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldAutoText::get_EntryName Methode. Gibt den Namen des AutoText‑Eintrags in C++ zurück oder legt ihn fest."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldautotext/get_entryname/
---
## FieldAutoText::get_EntryName method


Liest oder setzt den Namen des AutoText-Eintrags.

```cpp
System::String Aspose::Words::Fields::FieldAutoText::get_EntryName() override
```


## Beispiele



Zeigt, wie man einen Baustein mit AUTOTEXT- und GLOSSARY-Feldern anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie ein Glossar-Dokument und fügen Sie einen AutoText-Baustein hinzu.
doc->set_GlossaryDocument(System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>());
auto buildingBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(doc->get_GlossaryDocument());
buildingBlock->set_Name(u"MyBlock");
buildingBlock->set_Gallery(Aspose::Words::BuildingBlocks::BuildingBlockGallery::AutoText);
buildingBlock->set_Category(u"General");
buildingBlock->set_Description(u"MyBlock description");
buildingBlock->set_Behavior(Aspose::Words::BuildingBlocks::BuildingBlockBehavior::Paragraph);
doc->get_GlossaryDocument()->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(buildingBlock);

// Erstellen Sie eine Quelle und fügen Sie sie als Text zu unserem Baustein hinzu.
auto buildingBlockSource = System::MakeObject<Aspose::Words::Document>();
auto buildingBlockSourceBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(buildingBlockSource);
buildingBlockSourceBuilder->Writeln(u"Hello World!");

System::SharedPtr<Aspose::Words::Node> buildingBlockContent = doc->get_GlossaryDocument()->ImportNode(buildingBlockSource->get_FirstSection(), true);
buildingBlock->AppendChild<System::SharedPtr<Aspose::Words::Node>>(buildingBlockContent);

// Legen Sie eine Datei fest, die Teile enthält, die unser Dokument oder seine angehängte Vorlage möglicherweise nicht enthält.
doc->get_FieldOptions()->set_BuiltInTemplatesPaths(System::MakeArray<System::String>({get_MyDir() + u"Busniess brochure.dotx"}));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Im Folgenden werden zwei Möglichkeiten gezeigt, Felder zu verwenden, um den Inhalt unseres Bausteins anzuzeigen.
// 1 -  Verwendung eines AUTOTEXT-Feldes:
auto fieldAutoText = System::ExplicitCast<Aspose::Words::Fields::FieldAutoText>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoText, true));
fieldAutoText->set_EntryName(u"MyBlock");

ASSERT_EQ(u" AUTOTEXT  MyBlock", fieldAutoText->GetFieldCode());

// 2 -  Verwendung eines GLOSSARY-Feldes:
auto fieldGlossary = System::ExplicitCast<Aspose::Words::Fields::FieldGlossary>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGlossary, true));
fieldGlossary->set_EntryName(u"MyBlock");

ASSERT_EQ(u" GLOSSARY  MyBlock", fieldGlossary->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.AUTOTEXT.GLOSSARY.dotx");
```

## Siehe auch

* Class [FieldAutoText](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
