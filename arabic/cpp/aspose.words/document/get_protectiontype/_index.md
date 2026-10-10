---
title: "طريقة Aspose::Words::Document::get_ProtectionType"
linktitle: "get_ProtectionType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_ProtectionType. يحصل على نوع حماية المستند النشط حاليًا في C++."
type: docs
weight: 44000
url: /ar/cpp/aspose.words/document/get_protectiontype/
---
## Document::get_ProtectionType method


يحصل على نوع حماية المستند النشط حاليًا.

```cpp
Aspose::Words::ProtectionType Aspose::Words::Document::get_ProtectionType()
```

## ملاحظات


تسمح هذه الخاصية باسترجاع نوع حماية المستند المحدد حاليًا. لتغيير نوع حماية المستند استخدم طريقتي [Protect()](../) و [Unprotect](../unprotect/).

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
