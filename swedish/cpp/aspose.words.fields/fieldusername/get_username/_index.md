---
title: "Aspose::Words::Fields::FieldUserName::get_UserName‑metoden"
linktitle: "get_UserName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldUserName::get_UserName‑metoden. Hämtar eller sätter det aktuella användarens namn i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldusername/get_username/
---
## FieldUserName::get_UserName method


Hämtar eller sätter den aktuella användarens namn.

```cpp
System::String Aspose::Words::Fields::FieldUserName::get_UserName()
```


## Exempel



Visar hur man använder USERNAME-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa ett UserInformation-objekt och ange det som källa för användarinformation för alla fält som vi skapar.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett USERNAME-fält för att visa den aktuella användarens namn,
// hämtat från UserInformation-objektet som vi skapade ovan.
auto fieldUserName = System::ExplicitCast<Aspose::Words::Fields::FieldUserName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserName, true));
ASSERT_EQ(userInformation->get_Name(), fieldUserName->get_Result());

ASSERT_EQ(u" USERNAME ", fieldUserName->GetFieldCode());
ASSERT_EQ(u"John Doe", fieldUserName->get_Result());

// Vi kan sätta den här egenskapen för att få vårt fält att åsidosätta värdet som för närvarande lagras i UserInformation-objektet.
fieldUserName->set_UserName(u"Jane Doe");
fieldUserName->Update();

ASSERT_EQ(u" USERNAME  \"Jane Doe\"", fieldUserName->GetFieldCode());
ASSERT_EQ(u"Jane Doe", fieldUserName->get_Result());

// Detta påverkar inte värdet i UserInformation-objektet.
ASSERT_EQ(u"John Doe", doc->get_FieldOptions()->get_CurrentUser()->get_Name());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERNAME.docx");
```

## Se även

* Class [FieldUserName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
