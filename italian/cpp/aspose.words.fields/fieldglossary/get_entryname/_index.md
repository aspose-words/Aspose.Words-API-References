---
title: "metodo Aspose::Words::Fields::FieldGlossary::get_EntryName"
linktitle: "get_EntryName"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Fields::FieldGlossary::get_EntryName. Ottiene o imposta il nome della voce del glossario da inserire in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldglossary/get_entryname/
---
## FieldGlossary::get_EntryName method


Ottiene o imposta il nome della voce del glossario da inserire.

```cpp
System::String Aspose::Words::Fields::FieldGlossary::get_EntryName() override
```


## Esempi



Mostra come visualizzare un blocco di costruzione con i campi AUTOTEXT e GLOSSARY.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un documento di glossario e aggiungi ad esso un blocco di costruzione AutoText.
doc->set_GlossaryDocument(System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>());
auto buildingBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(doc->get_GlossaryDocument());
buildingBlock->set_Name(u"MyBlock");
buildingBlock->set_Gallery(Aspose::Words::BuildingBlocks::BuildingBlockGallery::AutoText);
buildingBlock->set_Category(u"General");
buildingBlock->set_Description(u"MyBlock description");
buildingBlock->set_Behavior(Aspose::Words::BuildingBlocks::BuildingBlockBehavior::Paragraph);
doc->get_GlossaryDocument()->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(buildingBlock);

// Crea una sorgente e aggiungila come testo al nostro blocco di costruzione.
auto buildingBlockSource = System::MakeObject<Aspose::Words::Document>();
auto buildingBlockSourceBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(buildingBlockSource);
buildingBlockSourceBuilder->Writeln(u"Hello World!");

System::SharedPtr<Aspose::Words::Node> buildingBlockContent = doc->get_GlossaryDocument()->ImportNode(buildingBlockSource->get_FirstSection(), true);
buildingBlock->AppendChild<System::SharedPtr<Aspose::Words::Node>>(buildingBlockContent);

// Imposta un file che contiene parti che il nostro documento, o il suo modello allegato, potrebbe non contenere.
doc->get_FieldOptions()->set_BuiltInTemplatesPaths(System::MakeArray<System::String>({get_MyDir() + u"Busniess brochure.dotx"}));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono due modi per utilizzare i campi per visualizzare il contenuto del nostro blocco di costruzione.
// 1 -  Utilizzo di un campo AUTOTEXT:
auto fieldAutoText = System::ExplicitCast<Aspose::Words::Fields::FieldAutoText>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoText, true));
fieldAutoText->set_EntryName(u"MyBlock");

ASSERT_EQ(u" AUTOTEXT  MyBlock", fieldAutoText->GetFieldCode());

// 2 -  Utilizzo di un campo GLOSSARY:
auto fieldGlossary = System::ExplicitCast<Aspose::Words::Fields::FieldGlossary>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGlossary, true));
fieldGlossary->set_EntryName(u"MyBlock");

ASSERT_EQ(u" GLOSSARY  MyBlock", fieldGlossary->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.AUTOTEXT.GLOSSARY.dotx");
```

## Vedi anche

* Class [FieldGlossary](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
