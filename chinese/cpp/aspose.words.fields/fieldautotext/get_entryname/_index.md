---
title: "Aspose::Words::Fields::FieldAutoText::get_EntryName 方法"
linktitle: "get_EntryName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldAutoText::get_EntryName 方法。获取或设置 AutoText 条目的名称（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldautotext/get_entryname/
---
## FieldAutoText::get_EntryName method


获取或设置 AutoText 条目的名称。

```cpp
System::String Aspose::Words::Fields::FieldAutoText::get_EntryName() override
```


## 示例



展示如何使用 AUTOTEXT 和 GLOSSARY 字段显示构建块。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建一个术语表文档并向其中添加 AutoText 构建块。
doc->set_GlossaryDocument(System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>());
auto buildingBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(doc->get_GlossaryDocument());
buildingBlock->set_Name(u"MyBlock");
buildingBlock->set_Gallery(Aspose::Words::BuildingBlocks::BuildingBlockGallery::AutoText);
buildingBlock->set_Category(u"General");
buildingBlock->set_Description(u"MyBlock description");
buildingBlock->set_Behavior(Aspose::Words::BuildingBlocks::BuildingBlockBehavior::Paragraph);
doc->get_GlossaryDocument()->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(buildingBlock);

// 创建一个源并将其作为文本添加到我们的构建块中。
auto buildingBlockSource = System::MakeObject<Aspose::Words::Document>();
auto buildingBlockSourceBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(buildingBlockSource);
buildingBlockSourceBuilder->Writeln(u"Hello World!");

System::SharedPtr<Aspose::Words::Node> buildingBlockContent = doc->get_GlossaryDocument()->ImportNode(buildingBlockSource->get_FirstSection(), true);
buildingBlock->AppendChild<System::SharedPtr<Aspose::Words::Node>>(buildingBlockContent);

// 设置一个文件，该文件包含我们的文档或其附加模板可能不包含的部分。
doc->get_FieldOptions()->set_BuiltInTemplatesPaths(System::MakeArray<System::String>({get_MyDir() + u"Busniess brochure.dotx"}));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 下面有两种使用字段显示我们构建块内容的方法。
// 1 - 使用 AUTOTEXT 字段：
auto fieldAutoText = System::ExplicitCast<Aspose::Words::Fields::FieldAutoText>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoText, true));
fieldAutoText->set_EntryName(u"MyBlock");

ASSERT_EQ(u" AUTOTEXT  MyBlock", fieldAutoText->GetFieldCode());

// 2 - 使用 GLOSSARY 字段：
auto fieldGlossary = System::ExplicitCast<Aspose::Words::Fields::FieldGlossary>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGlossary, true));
fieldGlossary->set_EntryName(u"MyBlock");

ASSERT_EQ(u" GLOSSARY  MyBlock", fieldGlossary->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.AUTOTEXT.GLOSSARY.dotx");
```

## 另见

* Class [FieldAutoText](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
