---
title: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials yöntemi"
linktitle: "get_UserInitials"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials yöntemi. C++'de geçerli kullanıcının baş harflerini alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fielduserinitials/get_userinitials/
---
## FieldUserInitials::get_UserInitials method


Geçerli kullanıcının baş harflerini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldUserInitials::get_UserInitials()
```


## Örnekler



USERINITIALS alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir UserInformation nesnesi oluşturun ve bunu oluşturduğumuz tüm alanlar için kullanıcı bilgisi kaynağı olarak ayarlayın.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Geçerli kullanıcının baş harflerini göstermek için bir USERINITIALS alanı oluşturun,
// yukarıda oluşturduğumuz UserInformation nesnesinden alınan.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<Aspose::Words::Fields::FieldUserInitials>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// Bu özelliği ayarlayarak alanımızın, UserInformation nesnesinde şu anda saklanan değeri geçersiz kılmasını sağlayabiliriz.
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// Bu, UserInformation nesnesindeki değeri etkilemez.
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERINITIALS.docx");
```

## Ayrıca Bakınız

* Class [FieldUserInitials](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
