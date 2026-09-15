---
title: "طريقة Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths"
linktitle: "get_BuiltInTemplatesPaths"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths. يحصل أو يضبط مسارات القوالب المدمجة في MS Word في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fields/fieldoptions/get_builtintemplatespaths/
---
## FieldOptions::get_BuiltInTemplatesPaths method


الحصول على أو تعيين مسارات القوالب المدمجة في MS Word.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths() const
```

## ملاحظات


هذه الخاصية تُستخدم من قبل حقلي [FieldAutoText](../../fieldautotext/) و [FieldGlossary](../../fieldglossary/)، إذا لم يُعثر على مدخل النص التلقائي المشار إليه في قالب [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/).

بشكل افتراضي، يخزن MS Word القوالب المدمجة في c:\Users\<username>\AppData\Roaming\**Microsoft**\[Document](../../../aspose.words/document/) Building Blocks\1033\16\Built-In Building Blocks.dotx و C:\Users\<username>\AppData\Roaming\**Microsoft**\Templates\Normal.dotm.

## أمثلة



يظهر كيفية عرض كتلة بناء باستخدام حقول AUTOTEXT و GLOSSARY.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أنشئ مستند مسرد وأضف إليه كتلة بناء AutoText.
doc->set_GlossaryDocument(System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>());
auto buildingBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(doc->get_GlossaryDocument());
buildingBlock->set_Name(u"MyBlock");
buildingBlock->set_Gallery(Aspose::Words::BuildingBlocks::BuildingBlockGallery::AutoText);
buildingBlock->set_Category(u"General");
buildingBlock->set_Description(u"MyBlock description");
buildingBlock->set_Behavior(Aspose::Words::BuildingBlocks::BuildingBlockBehavior::Paragraph);
doc->get_GlossaryDocument()->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(buildingBlock);

// أنشئ مصدرًا وأضفه كنص إلى كتلة البناء الخاصة بنا.
auto buildingBlockSource = System::MakeObject<Aspose::Words::Document>();
auto buildingBlockSourceBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(buildingBlockSource);
buildingBlockSourceBuilder->Writeln(u"Hello World!");

System::SharedPtr<Aspose::Words::Node> buildingBlockContent = doc->get_GlossaryDocument()->ImportNode(buildingBlockSource->get_FirstSection(), true);
buildingBlock->AppendChild<System::SharedPtr<Aspose::Words::Node>>(buildingBlockContent);

// حدد ملفًا يحتوي على أجزاء قد لا يحتويها مستندنا أو القالب المرفق به.
doc->get_FieldOptions()->set_BuiltInTemplatesPaths(System::MakeArray<System::String>({get_MyDir() + u"Busniess brochure.dotx"}));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي طريقتان لاستخدام الحقول لعرض محتويات كتلة البناء الخاصة بنا.
// 1 -  باستخدام حقل AUTOTEXT:
auto fieldAutoText = System::ExplicitCast<Aspose::Words::Fields::FieldAutoText>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoText, true));
fieldAutoText->set_EntryName(u"MyBlock");

ASSERT_EQ(u" AUTOTEXT  MyBlock", fieldAutoText->GetFieldCode());

// 2 -  باستخدام حقل GLOSSARY:
auto fieldGlossary = System::ExplicitCast<Aspose::Words::Fields::FieldGlossary>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGlossary, true));
fieldGlossary->set_EntryName(u"MyBlock");

ASSERT_EQ(u" GLOSSARY  MyBlock", fieldGlossary->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.AUTOTEXT.GLOSSARY.dotx");
```

## انظر أيضًا

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
