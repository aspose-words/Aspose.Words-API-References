---
title: "метод Aspose::Words::Fields::FieldGlossary::get_EntryName"
linktitle: "get_EntryName"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Fields::FieldGlossary::get_EntryName. Получает или задает имя записи глоссария для вставки в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldglossary/get_entryname/
---
## FieldGlossary::get_EntryName method


Получает или задаёт имя записи глоссария для вставки.

```cpp
System::String Aspose::Words::Fields::FieldGlossary::get_EntryName() override
```


## Примеры



Показывает, как отобразить строительный блок с полями AUTOTEXT и GLOSSARY.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте документ глоссария и добавьте в него строительный блок AutoText.
doc->set_GlossaryDocument(System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>());
auto buildingBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(doc->get_GlossaryDocument());
buildingBlock->set_Name(u"MyBlock");
buildingBlock->set_Gallery(Aspose::Words::BuildingBlocks::BuildingBlockGallery::AutoText);
buildingBlock->set_Category(u"General");
buildingBlock->set_Description(u"MyBlock description");
buildingBlock->set_Behavior(Aspose::Words::BuildingBlocks::BuildingBlockBehavior::Paragraph);
doc->get_GlossaryDocument()->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(buildingBlock);

// Создайте источник и добавьте его в виде текста в наш строительный блок.
auto buildingBlockSource = System::MakeObject<Aspose::Words::Document>();
auto buildingBlockSourceBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(buildingBlockSource);
buildingBlockSourceBuilder->Writeln(u"Hello World!");

System::SharedPtr<Aspose::Words::Node> buildingBlockContent = doc->get_GlossaryDocument()->ImportNode(buildingBlockSource->get_FirstSection(), true);
buildingBlock->AppendChild<System::SharedPtr<Aspose::Words::Node>>(buildingBlockContent);

// Установите файл, который содержит части, которые наш документ или его прикреплённый шаблон могут не содержать.
doc->get_FieldOptions()->set_BuiltInTemplatesPaths(System::MakeArray<System::String>({get_MyDir() + u"Busniess brochure.dotx"}));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два способа использовать поля для отображения содержимого нашего строительного блока.
// 1 -  Использование поля AUTOTEXT:
auto fieldAutoText = System::ExplicitCast<Aspose::Words::Fields::FieldAutoText>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoText, true));
fieldAutoText->set_EntryName(u"MyBlock");

ASSERT_EQ(u" AUTOTEXT  MyBlock", fieldAutoText->GetFieldCode());

// 2 -  Использование поля GLOSSARY:
auto fieldGlossary = System::ExplicitCast<Aspose::Words::Fields::FieldGlossary>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGlossary, true));
fieldGlossary->set_EntryName(u"MyBlock");

ASSERT_EQ(u" GLOSSARY  MyBlock", fieldGlossary->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.AUTOTEXT.GLOSSARY.dotx");
```

## См. также

* Class [FieldGlossary](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
