---
title: Aspose::Words::Fields::FieldOptions::get_CurrentUser method
linktitle: get_CurrentUser
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions::get_CurrentUser method. Gets or sets the current user information in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fields/fieldoptions/get_currentuser/
---
## FieldOptions::get_CurrentUser method


Gets or sets the current user information.

```cpp
const System::SharedPtr<Aspose::Words::Fields::UserInformation> & Aspose::Words::Fields::FieldOptions::get_CurrentUser() const
```

## Examples


Shows how to set user details, and display them using fields.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Create a UserInformation object and set it as the data source for fields that display user information.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
// the respective properties of the UserInformation object that we have created above.
ASSERT_EQ(builder->InsertField(u" USERNAME ")->get_Result(), userInformation->get_Name());
ASSERT_EQ(builder->InsertField(u" USERINITIALS ")->get_Result(), userInformation->get_Initials());
ASSERT_EQ(builder->InsertField(u" USERADDRESS ")->get_Result(), userInformation->get_Address());

// The field options object also has a static default user that fields from all documents can refer to.
UserInformation::get_DefaultUser()->set_Name(u"Default User");
UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(UserInformation::get_DefaultUser());

ASSERT_EQ(builder->InsertField(u" USERNAME ")->get_Result(), u"Default User");
ASSERT_EQ(builder->InsertField(u" USERINITIALS ")->get_Result(), u"D. U.");
ASSERT_EQ(builder->InsertField(u" USERADDRESS ")->get_Result(), u"One Microsoft Way");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```
## See Also

* Class [UserInformation](../../userinformation/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
