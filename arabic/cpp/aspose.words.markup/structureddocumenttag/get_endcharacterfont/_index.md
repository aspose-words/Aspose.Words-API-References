---
title: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_EndCharacterFont method"
linktitle: "get_EndCharacterFont"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_EndCharacterFont method. تنسيق الخط الذي سيُطبق على الحرف الأخير من النص المدخل في SDT في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/get_endcharacterfont/
---
## StructuredDocumentTag::get_EndCharacterFont method


[Font](../../../aspose.words/font/) formatting that will be applied to the last character of text entered into **SDT**.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Markup::StructuredDocumentTag::get_EndCharacterFont()
```


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

* Class [Font](../../../aspose.words/font/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
