---
title: "Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths-Methode"
linktitle: "get_BuiltInTemplatesPaths"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths-Methode. Ruft Pfade zu den integrierten MS‑Word‑Vorlagen ab oder legt sie fest in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldoptions/get_builtintemplatespaths/
---
## FieldOptions::get_BuiltInTemplatesPaths method


Liest oder setzt Pfade zu den integrierten MS‑Word‑Vorlagen.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths() const
```

## Hinweise


Diese Eigenschaft wird von den Feldern [FieldAutoText](../../fieldautotext/) und [FieldGlossary](../../fieldglossary/) verwendet, falls der referenzierte Auto‑Text‑Eintrag in der [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/)-Vorlage nicht gefunden wird.

Standardmäßig speichert MS Word integrierte Vorlagen in c:\\Users\\<username>\\AppData\\Roaming\\**Microsoft**\\[Document](../../../aspose.words/document/) Building Blocks\\1033\\16\\Built-In Building Blocks.dotx und C:\\Users\\<username>\\AppData\\Roaming\\**Microsoft**\\Templates\\Normal.dotm‑Dateien.

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

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
