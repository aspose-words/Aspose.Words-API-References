---
title: "Aspose::Words::Fields::FieldAutoText::get_EntryName yöntemi"
linktitle: "get_EntryName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldAutoText::get_EntryName yöntemi. AutoText girişinin adını C++'ta alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldautotext/get_entryname/
---
## FieldAutoText::get_EntryName method


AutoText girişinin adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldAutoText::get_EntryName() override
```


## Örnekler



AUTOTEXT ve GLOSSARY alanlarıyla bir yapı bloğunu nasıl görüntüleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir sözlük belgesi oluşturun ve ona bir AutoText yapı bloğu ekleyin.
doc->set_GlossaryDocument(System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>());
auto buildingBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(doc->get_GlossaryDocument());
buildingBlock->set_Name(u"MyBlock");
buildingBlock->set_Gallery(Aspose::Words::BuildingBlocks::BuildingBlockGallery::AutoText);
buildingBlock->set_Category(u"General");
buildingBlock->set_Description(u"MyBlock description");
buildingBlock->set_Behavior(Aspose::Words::BuildingBlocks::BuildingBlockBehavior::Paragraph);
doc->get_GlossaryDocument()->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(buildingBlock);

// Bir kaynak oluşturun ve onu yapı bloğumuza metin olarak ekleyin.
auto buildingBlockSource = System::MakeObject<Aspose::Words::Document>();
auto buildingBlockSourceBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(buildingBlockSource);
buildingBlockSourceBuilder->Writeln(u"Hello World!");

System::SharedPtr<Aspose::Words::Node> buildingBlockContent = doc->get_GlossaryDocument()->ImportNode(buildingBlockSource->get_FirstSection(), true);
buildingBlock->AppendChild<System::SharedPtr<Aspose::Words::Node>>(buildingBlockContent);

// Belgemizin veya ekli şablonunun içermeyebileceği bölümleri içeren bir dosya ayarlayın.
doc->get_FieldOptions()->set_BuiltInTemplatesPaths(System::MakeArray<System::String>({get_MyDir() + u"Busniess brochure.dotx"}));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda, yapı bloğumuzun içeriğini görüntülemek için alanları kullanmanın iki yolu verilmiştir.
// 1 -  AUTOTEXT alanı kullanarak:
auto fieldAutoText = System::ExplicitCast<Aspose::Words::Fields::FieldAutoText>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoText, true));
fieldAutoText->set_EntryName(u"MyBlock");

ASSERT_EQ(u" AUTOTEXT  MyBlock", fieldAutoText->GetFieldCode());

// 2 -  GLOSSARY alanı kullanarak:
auto fieldGlossary = System::ExplicitCast<Aspose::Words::Fields::FieldGlossary>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGlossary, true));
fieldGlossary->set_EntryName(u"MyBlock");

ASSERT_EQ(u" GLOSSARY  MyBlock", fieldGlossary->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.AUTOTEXT.GLOSSARY.dotx");
```

## Ayrıca Bakınız

* Class [FieldAutoText](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
