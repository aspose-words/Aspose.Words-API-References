---
title: "طريقة Aspose::Words::Markup::StructuredDocumentTag::Clear"
linktitle: "Clear"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTag::Clear. تمسح محتويات هذا الوسم المهيكل للوثيقة وتعرض عنصرًا نائبًا إذا تم تعريفه في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag::Clear method


يمسح محتويات هذه العلامة المُنظمة ويعرض عنصرًا نائبًا إذا تم تعريفه.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::Clear()
```

## ملاحظات


ليس من الممكن مسح محتويات وسم مهيكل للوثيقة إذا كان يحتوي على مراجعات.

إذا تم ربط هذا الوسم المهيكل للوثيقة بـ XML مخصص (باستخدام خاصية [XmlMapping](../get_xmlmapping/))، يتم مسح عقدة XML المشار إليها.

## أمثلة



يعرض كيفية حذف محتويات عناصر الوسم المهيكل للوثيقة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أنشئ وسم مهيكل للوثيقة بنص عادي، ثم أضفه إلى المستند.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// هذا الوسم المهيكل للوثيقة، الذي يكون على شكل مربع نص، يعرض بالفعل نصًا نائبًا.
ASSERT_EQ(u"Click here to enter text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// أنشئ كتلة بناء بمحتوى نصي.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();
auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"My placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->EnsureMinimum();
substituteBlock->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(glossaryDoc, u"Custom placeholder text."));
glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// قم بتعيين خاصية "PlaceholderName" للوسم المهيكل للوثيقة إلى اسم كتلة البناء الخاصة بنا للحصول على
// الوسم المهيكل للوثيقة لعرض محتويات كتلة البناء بدلاً من النص الافتراضي الأصلي.
tag->set_PlaceholderName(u"My placeholder");

ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
ASSERT_TRUE(tag->get_IsShowingPlaceholderText());

// حرّر نص الوسم المهيكل للوثيقة وأخفِ النص النائب.
auto run = System::ExplicitCast<Aspose::Words::Run>(tag->GetChild(Aspose::Words::NodeType::Run, 0, true));
run->set_Text(u"New text.");
tag->set_IsShowingPlaceholderText(false);

ASSERT_EQ(u"New text.", tag->GetText().Trim());

// استخدم طريقة "Clear" لمسح محتويات هذا الوسم المهيكل للوثيقة وعرض النص النائب مرة أخرى.
tag->Clear();

ASSERT_TRUE(tag->get_IsShowingPlaceholderText());
ASSERT_EQ(u"Custom placeholder text.", tag->GetText().Trim());
```

## انظر أيضًا

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
