---
title: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress metod"
linktitle: "get_UserAddress"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress metod. Hämtar eller anger den aktuella användarens postadress i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fielduseraddress/get_useraddress/
---
## FieldUserAddress::get_UserAddress method


Hämtar eller anger den aktuella användarens postadress.

```cpp
System::String Aspose::Words::Fields::FieldUserAddress::get_UserAddress()
```


## Exempel



Visar hur man använder USERADDRESS-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa ett UserInformation-objekt och ange det som källa för användarinformation för alla fält som vi skapar.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Skapa ett USERADDRESS-fält för att visa den aktuella användarens adress,
// hämtat från UserInformation-objektet som vi skapade ovan.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<Aspose::Words::Fields::FieldUserAddress>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserAddress, true));

ASSERT_EQ(u" USERADDRESS ", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"123 Main Street", fieldUserAddress->get_Result());

// Vi kan sätta den här egenskapen för att få vårt fält att åsidosätta värdet som för närvarande lagras i UserInformation-objektet.
fieldUserAddress->set_UserAddress(u"456 North Road");
fieldUserAddress->Update();

ASSERT_EQ(u" USERADDRESS  \"456 North Road\"", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"456 North Road", fieldUserAddress->get_Result());

// Detta påverkar inte värdet i UserInformation-objektet.
ASSERT_EQ(u"123 Main Street", doc->get_FieldOptions()->get_CurrentUser()->get_Address());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERADDRESS.docx");
```

## Se även

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
