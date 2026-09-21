---
title: "Aspose::Words::Fields::UserInformation::get_Name metod"
linktitle: "get_Name"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::UserInformation::get_Name metod. Hämtar eller anger användarens namn i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.fields/userinformation/get_name/
---
## UserInformation::get_Name method


Hämtar eller anger användarens namn.

```cpp
System::String Aspose::Words::Fields::UserInformation::get_Name() const
```


## Exempel



Visar hur man ställer in användardetaljer och visar dem med fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett UserInformation-objekt och ange det som datakälla för fält som visar användarinformation.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Infoga fälten USERNAME, USERINITIALS och USERADDRESS, som visar värden av
// de respektive egenskaperna i UserInformation-objektet som vi skapade ovan.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// Fältalternativobjektet har också en statisk standardanvändare som fält från alla dokument kan referera till.
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

## Se även

* Class [UserInformation](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
