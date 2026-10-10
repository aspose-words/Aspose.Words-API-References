---
title: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials metod"
linktitle: "get_UserInitials"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials metod. Hämtar eller anger den aktuella användarens initialer i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fielduserinitials/get_userinitials/
---
## FieldUserInitials::get_UserInitials method


Hämtar eller anger den aktuella användarens initialer.

```cpp
System::String Aspose::Words::Fields::FieldUserInitials::get_UserInitials()
```


## Exempel



Visar hur man använder USERINITIALS-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa ett UserInformation-objekt och ange det som källa för användarinformation för alla fält som vi skapar.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Skapa ett USERINITIALS-fält för att visa den aktuella användarens initialer,
// hämtat från UserInformation-objektet som vi skapade ovan.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<Aspose::Words::Fields::FieldUserInitials>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// Vi kan sätta den här egenskapen för att få vårt fält att åsidosätta värdet som för närvarande lagras i UserInformation-objektet.
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// Detta påverkar inte värdet i UserInformation-objektet.
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERINITIALS.docx");
```

## Se även

* Class [FieldUserInitials](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
