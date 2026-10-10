---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary طريقة"
linktitle: "get_IsTemporary"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary طريقة. يحدد ما إذا كان يجب إزالة هذا الـ SDT من مستند WordProcessingML عندما يتم تعديل محتوياته في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/get_istemporary/
---
## StructuredDocumentTag::get_IsTemporary method


يحدد ما إذا كانت هذه **SDT** ستُزال من مستند WordProcessingML عندما يتم تعديل محتوياتها.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary() const
```


## أمثلة



يوضح كيفية إنشاء عناصر تحكم للاستخدام الواحد.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أدرج علامة مستند منظم بنص عادي،
// والتي ستعمل كنموذج نص عادي يمكن للمستخدم إدخال النص فيه.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// قم بتعيين الخاصية "IsTemporary" إلى "true" لجعل علامة المستند المنظم تختفي و
// دمج محتوياتها في المستند بعد أن يقوم المستخدم بتحريرها مرة واحدة في Microsoft Word.
// قم بتعيين الخاصية "IsTemporary" إلى "false" للسماح للمستخدم بتحرير المحتويات
// لعلامة المستند المنظم عددًا غير محدود من المرات.
tag->set_IsTemporary(isTemporary);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Please enter text: ");
builder->InsertNode(tag);

// أدرج علامة مستند منظم أخرى على شكل مربع اختيار وضع الحالة الافتراضية إلى "checked".
tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
tag->set_Checked(true);

// قم بتعيين الخاصية "IsTemporary" إلى "true" لجعل مربع الاختيار يتحول إلى رمز
// بعد أن ينقر المستخدم عليه في Microsoft Word.
// قم بتعيين الخاصية "IsTemporary" إلى "false" للسماح للمستخدم بالنقر على مربع الاختيار عددًا غير محدود من المرات.
tag->set_IsTemporary(isTemporary);

builder->Write(u"\nPlease click the check box: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IsTemporary.docx");
```

## انظر أيضًا

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
