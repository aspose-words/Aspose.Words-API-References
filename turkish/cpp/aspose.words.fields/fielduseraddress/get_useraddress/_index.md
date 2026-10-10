---
title: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress metodu"
linktitle: "get_UserAddress"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress metodu. C++'ta geçerli kullanıcının posta adresini alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fielduseraddress/get_useraddress/
---
## FieldUserAddress::get_UserAddress method


Geçerli kullanıcının posta adresini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldUserAddress::get_UserAddress()
```


## Örnekler



USERADDRESS alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir UserInformation nesnesi oluşturun ve bunu oluşturduğumuz tüm alanlar için kullanıcı bilgisi kaynağı olarak ayarlayın.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Geçerli kullanıcının adresini göstermek için bir USERADDRESS alanı oluşturun,
// yukarıda oluşturduğumuz UserInformation nesnesinden alınan.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<Aspose::Words::Fields::FieldUserAddress>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserAddress, true));

ASSERT_EQ(u" USERADDRESS ", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"123 Main Street", fieldUserAddress->get_Result());

// Bu özelliği ayarlayarak alanımızın, UserInformation nesnesinde şu anda saklanan değeri geçersiz kılmasını sağlayabiliriz.
fieldUserAddress->set_UserAddress(u"456 North Road");
fieldUserAddress->Update();

ASSERT_EQ(u" USERADDRESS  \"456 North Road\"", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"456 North Road", fieldUserAddress->get_Result());

// Bu, UserInformation nesnesindeki değeri etkilemez.
ASSERT_EQ(u"123 Main Street", doc->get_FieldOptions()->get_CurrentUser()->get_Address());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERADDRESS.docx");
```

## Ayrıca Bakınız

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
