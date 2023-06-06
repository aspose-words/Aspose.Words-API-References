---
title: Aspose::Words::Fields::FieldUserInitials::get_UserInitials method
linktitle: get_UserInitials
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldUserInitials::get_UserInitials method. Gets or sets the current user''s initials in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fielduserinitials/get_userinitials/
---
## FieldUserInitials::get_UserInitials method


Gets or sets the current user's initials.

```cpp
System::String Aspose::Words::Fields::FieldUserInitials::get_UserInitials()
```


## Examples



Shows how to use the USERINITIALS field. 
```cpp
auto doc = MakeObject<Document>();

// Create a UserInformation object and set it as the source of user information for any fields that we create.
auto userInformation = MakeObject<UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Create a USERINITIALS field to display the current user's initials,
// taken from the UserInformation object we created above.
auto builder = MakeObject<DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<FieldUserInitials>(builder->InsertField(FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// We can set this property to get our field to override the value currently stored in the UserInformation object.
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// This does not affect the value in the UserInformation object.
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.USERINITIALS.docx");
```

## See Also

* Class [FieldUserInitials](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
