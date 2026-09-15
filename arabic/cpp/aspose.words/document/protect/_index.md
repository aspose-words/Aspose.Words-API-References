---
title: "Aspose::Words::Document::Protect طريقة"
linktitle: "حماية"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::Protect طريقة. يحمي المستند من التغييرات دون تغيير كلمة المرور الحالية أو يعيّن كلمة مرور عشوائية في C++."
type: docs
weight: 67000
url: /ar/cpp/aspose.words/document/protect/
---
## Document::Protect(Aspose::Words::ProtectionType) method


يحمي المستند من التغييرات دون تغيير كلمة المرور الحالية أو يعيّن كلمة مرور عشوائية.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| نوع | Aspose::Words::ProtectionType | يحدد نوع الحماية للمستند. |
## ملاحظات


عند حماية المستند، يمكن للمستخدم إجراء تغييرات محدودة فقط، مثل إضافة تعليقات، إجراء مراجعات، أو إكمال نموذج.

عند حماية مستند، وإذا كان المستند يحتوي بالفعل على كلمة مرور حماية، فإن كلمة المرور الحالية لا تتغير.

عند حماية مستند، وإذا لم يكن للمستند كلمة مرور حماية، تقوم هذه الطريقة بتعيين كلمة مرور عشوائية تجعل من المستحيل إلغاء حماية المستند في Microsoft Word، ولكن لا يزال بإمكانك إلغاء حماية المستند في Aspose.Words لأنها لا تتطلب كلمة مرور عند الإلغاء.

## أمثلة



يظهر كيفية إيقاف الحماية لقسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// تطبيق حماية كتابة على كل قسم في المستند.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// إيقاف حماية الكتابة للقسم الأول.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// في مستند الإخراج هذا، سنتمكن من تحرير القسم الأول بحرية،
// وسنتمكن فقط من تحرير محتويات حقل النموذج في القسم الثاني.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## انظر أيضًا

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Protect(Aspose::Words::ProtectionType, const System::String\&) method


يحمي المستند من التغييرات ويحدد اختياريًا كلمة مرور الحماية.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type, const System::String &password)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| نوع | Aspose::Words::ProtectionType | يحدد نوع الحماية للمستند. |
| password | const System::String\& | كلمة المرور المستخدمة لحماية المستند. حدد **null** أو سلسلة فارغة إذا أردت حماية المستند بدون كلمة مرور. |
## ملاحظات


عند حماية المستند، يمكن للمستخدم إجراء تغييرات محدودة فقط، مثل إضافة تعليقات، إجراء مراجعات، أو إكمال نموذج.

لاحظ أن حماية المستند تختلف عن حماية الكتابة. يتم تحديد حماية الكتابة باستخدام [WriteProtection](../get_writeprotection/).

## أمثلة



يظهر كيفية حماية وإلغاء حماية المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"password");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// إذا فتحنا هذا المستند باستخدام Microsoft Word بنية تحريره،
// سيتعين علينا إدخال كلمة المرور لتجاوز الحماية.
doc->Save(get_ArtifactsDir() + u"Document.Protect.docx");

// لاحظ أن الحماية تنطبق فقط على مستخدمي Microsoft Word الذين يفتحون مستندنا.
// لم نقم بتشفير المستند بأي شكل، ولا نحتاج إلى كلمة المرور لفتحها وتحريرها برمجيًا.
auto protectedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.Protect.docx");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// هناك طريقتان لإزالة الحماية من المستند.
// 1 - بدون كلمة مرور:
doc->Unprotect();

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - باستخدام كلمة المرور الصحيحة:
doc->Unprotect(u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());
```

## انظر أيضًا

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
