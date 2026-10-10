---
title: "Aspose::Words::Fields::UserInformation::get_DefaultUser yöntemi"
linktitle: "get_DefaultUser"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::UserInformation::get_DefaultUser yöntemi. C++'ta varsayılan kullanıcı bilgileri."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.fields/userinformation/get_defaultuser/
---
## UserInformation::get_DefaultUser method


Varsayılan kullanıcı bilgileri.

```cpp
static System::SharedPtr<Aspose::Words::Fields::UserInformation> Aspose::Words::Fields::UserInformation::get_DefaultUser()
```


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

* Class [UserInformation](../)
* Class [UserInformation](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
