---
title: "Aspose::Words::Properties::DocumentSecurity enum"
linktitle: "DocumentSecurity"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::DocumentSecurity enum. Security özelliği için bir değer olarak kullanılır. Bir belgenin güvenlik seviyesini sayısal bir değer olarak C++'da belirtir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enum


[Security](../builtindocumentproperties/get_security/) özelliği için bir değer olarak kullanılır. Bir belgenin güvenlik seviyesini sayısal bir değer olarak belirtir.

```cpp
enum class DocumentSecurity
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Özellik tarafından belirtilen güvenlik durumu yoktur. |
| PasswordProtected | 1 | Belge şifre korumalıdır. (Şu ana kadar bir belgede hiç görülmemiştir.) |
| ReadOnlyRecommended | 2 | Belge mümkünse salt okunur olarak açılacak, ancak ayar geçersiz kılınabilir. |
| ReadOnlyEnforced | 4 | Belge her zaman salt okunur olarak açılacak. |
| ReadOnlyExceptAnnotations | 8 | Belge, ek açıklamalar hariç, her zaman salt okunur olarak açılacak. |


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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
