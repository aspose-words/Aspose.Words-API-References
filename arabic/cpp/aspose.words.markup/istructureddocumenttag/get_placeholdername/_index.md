---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName طريقة"
linktitle: "get_PlaceholderName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName طريقة. يحصل على أو يعيّن اسم الـ BuildingBlock الذي يحتوي على نص العنصر النائب في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.markup/istructureddocumenttag/get_placeholdername/
---
## IStructuredDocumentTag::get_PlaceholderName method


يحصل أو يعيّن اسم الـ [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) الذي يحتوي على نص العنصر النائب.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName()=0
```


## أمثلة



يظهر كيفية استخدام محتويات كتلة البناء كنص عنصر نائب مخصص لعلامة مستند منسقة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أدرج علامة مستند منسقة بنص عادي من النوع "PlainText"، والتي ستعمل كصندوق نص.
// المحتويات التي سيعرضها بشكل افتراضي هي مطالبة "Click here to enter text.".
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// يمكننا جعل العلامة تعرض محتويات كتلة بناء بدلاً من النص الافتراضي.
// أولاً، أضف كتلة بناء تحتوي على محتويات إلى مستند القاموس.
System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossaryDoc = doc->get_GlossaryDocument();

auto substituteBlock = System::MakeObject<Aspose::Words::BuildingBlocks::BuildingBlock>(glossaryDoc);
substituteBlock->set_Name(u"Custom Placeholder");
substituteBlock->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(glossaryDoc));
substituteBlock->get_FirstSection()->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(glossaryDoc));
substituteBlock->get_FirstSection()->get_Body()->AppendParagraph(u"Custom placeholder text.");

glossaryDoc->AppendChild<System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock>>(substituteBlock);

// ثم، استخدم خاصية "PlaceholderName" لعلامة المستند المنسقة للإشارة إلى تلك كتلة البناء بالاسم.
tag->set_PlaceholderName(u"Custom Placeholder");

// إذا كانت "PlaceholderName" تشير إلى كتلة موجودة في مستند القاموس للمستند الأصلي،
// سيمكننا التحقق من كتلة البناء عبر خاصية "Placeholder".
ASPOSE_ASSERT_EQ(substituteBlock, tag->get_Placeholder());

// اضبط خاصية "IsShowingPlaceholderText" إلى "true" لتعامل الـ
// محتويات علامة المستند المنسقة الحالية كنص عنصر نائب.
// هذا يعني أن النقر على صندوق النص في Microsoft Word سيُبرز فوراً جميع محتويات العلامة.
// اضبط خاصية "IsShowingPlaceholderText" إلى "false" للحصول على الـ
// علامة المستند المنسقة لتعامل محتوياتها كنص أدخله المستخدم مسبقاً.
// النقر على هذا النص في Microsoft Word سيضع المؤشر اللامع في الموقع الذي تم النقر عليه.
tag->set_IsShowingPlaceholderText(isShowingPlaceholderText);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

## انظر أيضًا

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
