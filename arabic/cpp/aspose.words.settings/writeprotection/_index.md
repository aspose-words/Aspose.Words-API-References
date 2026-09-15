---
title: "فئة Aspose::Words::Settings::WriteProtection"
linktitle: "WriteProtection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Settings::WriteProtection. تحدد إعدادات الحماية من الكتابة للمستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.settings/writeprotection/
---
## WriteProtection class


يحدد إعدادات الحماية من الكتابة للمستند. لمعرفة المزيد، زر مقالة الوثائق [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class WriteProtection : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_IsWriteProtected](./get_iswriteprotected/)() | يرجع **true** عندما يتم تعيين كلمة مرور الحماية من الكتابة. |
| [get_ReadOnlyRecommended](./get_readonlyrecommended/)() const | يحدد ما إذا كان مؤلف المستند قد أوصى بفتح المستند للقراءة فقط. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ReadOnlyRecommended](./set_readonlyrecommended/)(bool) | مُعيّن لـ [Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended](./get_readonlyrecommended/). |
| [SetPassword](./setpassword/)(const System::String\&) | يضبط كلمة مرور الحماية من الكتابة للمستند. |
| static [Type](./type/)() |  |
| [ValidatePassword](./validatepassword/)(const System::String\&) | يرجع **true** إذا كانت كلمة المرور المحددة هي نفسها كلمة مرور الحماية من الكتابة التي تم حماية المستند بها. إذا لم يكن المستند محمياً من الكتابة بكلمة مرور، فإنّه يرجع **false**. |
## ملاحظات


تحدد الحماية من الكتابة ما إذا كان المؤلف قد أوصى بفتح المستند للقراءة فقط و/أو طلب كلمة مرور لتعديل المستند.

حماية الكتابة تختلف عن حماية المستند. يتم تحديد حماية الكتابة في Microsoft Word ضمن خيارات مربع الحوار حفظ باسم.

أنت لا تنشئ مثيلات من هذه الفئة مباشرة. يمكنك الوصول إلى إعدادات حماية المستند عبر الخاصية [WriteProtection](../../aspose.words/document/get_writeprotection/).

## أمثلة



يوضح كيفية حماية مستند باستخدام كلمة مرور.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// أدخل كلمة مرور بطول يصل إلى 15 حرفًا، ثم تحقق من حالة حماية المستند.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// الحماية لا تمنع تحرير المستند برمجيًا، ولا تشفر المحتويات.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## انظر أيضًا

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
