---
title: "طريقة Aspose::Words::Document::Unprotect"
linktitle: "إلغاء الحماية"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::Unprotect. تزيل الحماية من المستند بغض النظر عن كلمة المرور في C++."
type: docs
weight: 95000
url: /ar/cpp/aspose.words/document/unprotect/
---
## Document::Unprotect() method


يزيل الحماية من المستند بغض النظر عن كلمة المرور.

```cpp
void Aspose::Words::Document::Unprotect()
```

## ملاحظات


هذه الطريقة تُلغي حماية المستند حتى إذا كان يحتوي على كلمة مرور حماية.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Unprotect(const System::String\&) method


يزيل الحماية من المستند إذا تم تحديد كلمة مرور صحيحة.

```cpp
bool Aspose::Words::Document::Unprotect(const System::String &password)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| password | const System::String\& | كلمة المرور المستخدمة لإلغاء حماية المستند. |

### ReturnValue

**true** if a correct password was specified and the document was unprotected.
## ملاحظات


تُلغي هذه الطريقة حماية المستند فقط إذا تم تحديد كلمة مرور صحيحة.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
