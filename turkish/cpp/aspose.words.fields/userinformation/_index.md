---
title: "Aspose::Words::Fields::UserInformation class"
linktitle: "UserInformation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::UserInformation sınıfı. Kullanıcı hakkında bilgi belirtir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 117000
url: /tr/cpp/aspose.words.fields/userinformation/
---
## UserInformation class


Kullanıcı hakkında bilgi belirtir. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class UserInformation : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Address](./get_address/)() const | Kullanıcının posta adresini alır veya ayarlar. |
| static [get_DefaultUser](./get_defaultuser/)() | Varsayılan kullanıcı bilgileri. |
| [get_Initials](./get_initials/)() const | Kullanıcının baş harflerini alır veya ayarlar. |
| [get_Name](./get_name/)() const | Kullanıcının adını alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Address](./set_address/)(const System::String\&) | [Aspose::Words::Fields::UserInformation::get_Address](./get_address/) için ayarlayıcı. |
| [set_Initials](./set_initials/)(const System::String\&) | [Aspose::Words::Fields::UserInformation::get_Initials](./get_initials/) için ayarlayıcı. |
| [set_Name](./set_name/)(const System::String\&) | [Aspose::Words::Fields::UserInformation::get_Name](./get_name/) için ayarlayıcı. |
| static [Type](./type/)() |  |
| [UserInformation](./userinformation/)() |  |

## Örnekler



Kullanıcı ayrıntılarını nasıl ayarlayacağınızı ve alanları kullanarak nasıl görüntüleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir UserInformation nesnesi oluşturun ve bunu kullanıcı bilgilerini görüntüleyen alanlar için veri kaynağı olarak ayarlayın.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// USERNAME, USERINITIALS ve USERADDRESS alanlarını ekleyin; bu alanlar değerlerini gösterir
// yukarıda oluşturduğumuz UserInformation nesnesinin ilgili özelliklerini.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// Alan seçenekleri nesnesi ayrıca tüm belgelerden alanların başvurabileceği statik bir varsayılan kullanıcı içerir.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
