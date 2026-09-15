---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Id method"
linktitle: "get_Id"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Id طريقة. تحدد معرفًا رقميًا فريدًا للقراءة فقط ومستمر لهذا الـ SDT في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/get_id/
---
## StructuredDocumentTag::get_Id method


يحدد معرفًا رقميًا فريدًا للقراءة فقط ومستمرًا لهذا **SDT**.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTag::get_Id() override
```

## ملاحظات


يجب أن تتبع سمة Id هذه القواعد:* يجب أن يحتفظ المستند بمعرفات SDT فقط إذا تم استنساخ المستند بالكامل [Clone](../../../aspose.words/document/clone/).
* During [ImportNode()](../) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
* If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone SDT [Clone()](../) operation new unique ID will be generated for the cloned SDT node.
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.



## أمثلة



يظهر كيفية إنشاء علامة مستند منسقة في مربع نص عادي وتعديل مظهرها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// إنشاء علامة مستند منسقة ستحتوي على نص عادي.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// ضبط العنوان ولون الإطار الذي يظهر عند تمرير الفأرة فوق علامة المستند المنسقة في Microsoft Word.
tag->set_Title(u"My plain text");
tag->set_Color(System::Drawing::Color::get_Magenta());

// تعيين علامة لهذه العلامة المستندية المنسقة، والتي يمكن الحصول عليها
// كعنصر XML يُسمى "tag"، مع السلسلة أدناه في خاصية "@val" الخاصة به.
tag->set_Tag(u"MyPlainTextSDT");

// كل علامة مستند منسقة لديها معرف فريد عشوائي.
ASSERT_TRUE(tag->get_Id() > 0);

// ضبط الخط للنص داخل علامة المستند المنسقة.
tag->get_ContentsFont()->set_Name(u"Arial");

// ضبط الخط للنص في نهاية علامة المستند المنسقة.
// أي نص نكتبه في جسم المستند بعد الخروج من العلامة باستخدام مفاتيح السهم سيستخدم هذا الخط.
tag->get_EndCharacterFont()->set_Name(u"Arial Black");

// بشكل افتراضي، تكون القيمة false وعند الضغط على Enter داخل علامة المستند المنسقة لا يحدث شيء.
// عند ضبطها على true، يمكن لعلامة المستند المنسقة لدينا أن تحتوي على عدة أسطر.

// اضبط خاصية "Multiline" إلى "false" للسماح فقط بالمحتويات
// لعلامة المستند المنسقة هذه لتغطية سطر واحد.
// اضبط خاصية "Multiline" إلى "true" للسماح للعلامة باحتواء عدة أسطر من المحتوى.
tag->set_Multiline(true);

// اضبط خاصية "Appearance" إلى "SdtAppearance.Tags" لإظهار العلامات حول المحتوى.
// بشكل افتراضي، تُظهر علامة المستند المهيكلة كصندوق حدود.
tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

// أدرج نسخة من علامة المستند المهيكلة في فقرة جديدة.
auto tagClone = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(System::ExplicitCast<Aspose::Words::Node>(tag)->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// استخدم الطريقة "RemoveSelfOnly" لإزالة علامة المستند المهيكلة، مع إبقاء محتوياتها في المستند.
tagClone->RemoveSelfOnly();

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlainText.docx");
```

## انظر أيضًا

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
