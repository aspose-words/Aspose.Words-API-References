---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security طريقة"
linktitle: "get_Security"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security طريقة. يحدد مستوى أمان المستند كقيمة رقمية في C++."
type: docs
weight: 25000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_security/
---
## BuiltInDocumentProperties::get_Security method


يحدد مستوى أمان المستند كقيمة رقمية.

```cpp
Aspose::Words::Properties::DocumentSecurity Aspose::Words::Properties::BuiltInDocumentProperties::get_Security()
```

## ملاحظات


استخدم هذه الخاصية لأغراض إعلامية فقط لأن Microsoft Word لا يضبط هذه الخاصية دائمًا. هذه الخاصية متاحة فقط في مستندات DOC و OOXML.

لحماية أو إلغاء حماية مستند استخدم طريقتي [Protect()](../) و [Unprotect](../../../aspose.words/document/unprotect/).

Aspose.Words يحدث هذه الخاصية إلى قيمة صحيحة قبل حفظ المستند.

## أمثلة



يوضح كيفية استخدام خصائص المستند لعرض مستوى الأمان للمستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// إذا قمنا بتكوين مستند للقراءة فقط، سيعرض هذه الحالة باستخدام الخاصية المدمجة "Security".
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyRecommended, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// احمِ المستند من الكتابة، ثم تحقق من مستوى أمانه.
doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyEnforced, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// "Security" هي خاصية وصفية. يمكننا تعديل قيمتها يدويًا.
doc = System::MakeObject<Aspose::Words::Document>();

doc->Protect(Aspose::Words::ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")->get_BuiltInDocumentProperties()->get_Security());
```

## انظر أيضًا

* Enum [DocumentSecurity](../../documentsecurity/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
