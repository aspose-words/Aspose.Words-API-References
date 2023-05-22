---
title: Aspose::Words::Fields::FieldUserName::get_UserName method
linktitle: get_UserName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldUserName::get_UserName method. Gest or sets the current user''s name in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldusername/get_username/
---
## FieldUserName::get_UserName method


Gest or sets the current user's name.

```cpp
System::String Aspose::Words::Fields::FieldUserName::get_UserName()
```


## Examples



Shows how to use the USERNAME field. 
```cpp
auto doc = MakeObject<Document>();

// Create a UserInformation object and set it as the source of user information for any fields that we create.
auto userInformation = MakeObject<UserInformation>();
userInformation->set_Name(u"John Doe");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

auto builder = MakeObject<DocumentBuilder>(doc);

// Create a USERNAME field to display the current user's name,
// taken from the UserInformation object we created above.
auto fieldUserName = System::ExplicitCast<FieldUserName>(builder->InsertField(FieldType::FieldUserName, true));
ASSERT_EQ(userInformation->get_Name(), fieldUserName->get_Result());

ASSERT_EQ(u" USERNAME ", fieldUserName->GetFieldCode());
ASSERT_EQ(u"John Doe", fieldUserName->get_Result());

// We can set this property to get our field to override the value currently stored in the UserInformation object.
fieldUserName->set_UserName(u"Jane Doe");
fieldUserName->Update();

ASSERT_EQ(u" USERNAME  \"Jane Doe\"", fieldUserName->GetFieldCode());
ASSERT_EQ(u"Jane Doe", fieldUserName->get_Result());

// This does not affect the value in the UserInformation object.
ASSERT_EQ(u"John Doe", doc->get_FieldOptions()->get_CurrentUser()->get_Name());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.USERNAME.docx");
```

## See Also

* Class [FieldUserName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
