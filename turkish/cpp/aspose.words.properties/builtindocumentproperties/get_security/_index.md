---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security metodu"
linktitle: "get_Security"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security metodu. Bir belgenin güvenlik seviyesini C++'da sayısal bir değer olarak belirtir."
type: docs
weight: 25000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_security/
---
## BuiltInDocumentProperties::get_Security method


Belgenin güvenlik seviyesini sayısal bir değer olarak belirtir.

```cpp
Aspose::Words::Properties::DocumentSecurity Aspose::Words::Properties::BuiltInDocumentProperties::get_Security()
```

## Açıklamalar


Bu özelliği yalnızca bilgilendirme amaçlı kullanın çünkü Microsoft Word her zaman bu özelliği ayarlamaz. Bu özellik yalnızca DOC ve OOXML belgelerinde mevcuttur.

Bir belgeyi korumak veya korumasını kaldırmak için [Protect()](../) ve [Unprotect](../../../aspose.words/document/unprotect/) metodlarını kullanın.

Aspose.Words, bir belgeyi kaydetmeden önce bu özelliği doğru bir değere günceller.

## Örnekler



Bir belgenin güvenlik seviyesini göstermek için belge özelliklerinin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// Bir belgeyi salt okunur olarak yapılandırırsak, bu durumu yerleşik \"Security\" özelliğiyle gösterir.
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyRecommended, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// Bir belgeyi yazma korumalı hale getirin ve ardından güvenlik seviyesini doğrulayın.
doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyEnforced, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// \"Security\" açıklayıcı bir özelliktir. Değerini manuel olarak düzenleyebiliriz.
doc = System::MakeObject<Aspose::Words::Document>();

doc->Protect(Aspose::Words::ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")->get_BuiltInDocumentProperties()->get_Security());
```

## Ayrıca Bakınız

* Enum [DocumentSecurity](../../documentsecurity/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
