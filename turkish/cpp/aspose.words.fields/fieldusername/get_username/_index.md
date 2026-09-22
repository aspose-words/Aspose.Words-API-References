---
title: "Aspose::Words::Fields::FieldUserName::get_UserName metodu"
linktitle: "get_UserName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldUserName::get_UserName metodu. C++'ta geçerli kullanıcının adını alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldusername/get_username/
---
## FieldUserName::get_UserName method


Geçerli kullanıcının adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldUserName::get_UserName()
```


## Örnekler



USERNAME alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir UserInformation nesnesi oluşturun ve bunu oluşturduğumuz tüm alanlar için kullanıcı bilgisi kaynağı olarak ayarlayın.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Geçerli kullanıcının adını göstermek için bir USERNAME alanı oluşturun,
// yukarıda oluşturduğumuz UserInformation nesnesinden alınan.
auto fieldUserName = System::ExplicitCast<Aspose::Words::Fields::FieldUserName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserName, true));
ASSERT_EQ(userInformation->get_Name(), fieldUserName->get_Result());

ASSERT_EQ(u" USERNAME ", fieldUserName->GetFieldCode());
ASSERT_EQ(u"John Doe", fieldUserName->get_Result());

// Bu özelliği ayarlayarak alanımızın, UserInformation nesnesinde şu anda saklanan değeri geçersiz kılmasını sağlayabiliriz.
fieldUserName->set_UserName(u"Jane Doe");
fieldUserName->Update();

ASSERT_EQ(u" USERNAME  \"Jane Doe\"", fieldUserName->GetFieldCode());
ASSERT_EQ(u"Jane Doe", fieldUserName->get_Result());

// Bu, UserInformation nesnesindeki değeri etkilemez.
ASSERT_EQ(u"John Doe", doc->get_FieldOptions()->get_CurrentUser()->get_Name());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERNAME.docx");
```

## Ayrıca Bakınız

* Class [FieldUserName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
