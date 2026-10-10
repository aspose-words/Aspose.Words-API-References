---
title: "Aspose::Words::Properties::DocumentSecurity تعداد"
linktitle: "DocumentSecurity"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::DocumentSecurity تعداد. يُستخدم كقيمة لخاصية Security. يحدد مستوى أمان المستند كقيمة رقمية في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enum


يُستخدم كقيمة لخاصية [Security](../builtindocumentproperties/get_security/). يحدد مستوى أمان المستند كقيمة رقمية.

```cpp
enum class DocumentSecurity
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | لا توجد حالات أمان محددة بواسطة الخاصية. |
| PasswordProtected | 1 | المستند محمي بكلمة مرور. (ملاحظة: لم يُرَ هذا أبداً في أي مستند حتى الآن). |
| ReadOnlyRecommended | 2 | المستند الذي يجب فتحه للقراءة فقط إذا أمكن، لكن يمكن تجاوز الإعداد. |
| ReadOnlyEnforced | 4 | المستند الذي يجب فتحه دائمًا للقراءة فقط. |
| ReadOnlyExceptAnnotations | 8 | المستند الذي يجب فتحه دائمًا للقراءة فقط باستثناء التعليقات. |


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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
