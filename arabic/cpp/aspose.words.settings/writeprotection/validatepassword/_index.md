---
title: "طريقة Aspose::Words::Settings::WriteProtection::ValidatePassword"
linktitle: "ValidatePassword"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Settings::WriteProtection::ValidatePassword. تُرجع true إذا كانت كلمة المرور المحددة هي نفسها كلمة مرور الحماية للكتابة التي تم حماية المستند بها. إذا لم يكن المستند محمياً بحماية كتابة باستخدام كلمة مرور، فإنها تُرجع false في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection::ValidatePassword method


يرجع **true** إذا كانت كلمة المرور المحددة هي نفسها كلمة مرور الحماية من الكتابة التي تم حماية المستند بها. إذا لم يكن المستند محمياً من الكتابة بكلمة مرور، فإنّه يرجع **false**.

```cpp
bool Aspose::Words::Settings::WriteProtection::ValidatePassword(const System::String &password)
```


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

* Class [WriteProtection](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
