---
title: Aspose::Words::Fields::UserInformation::get_Name method
linktitle: get_Name
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::UserInformation::get_Name method. Gets or sets the user''s name in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.fields/userinformation/get_name/
---
## UserInformation::get_Name method


Gets or sets the user's name.

```cpp
System::String Aspose::Words::Fields::UserInformation::get_Name() const
```


## Examples



Shows how to set user details, and display them using fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a UserInformation object and set it as the data source for fields that display user information.
auto userInformation = MakeObject<UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
// the respective properties of the UserInformation object that we have created above.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// The field options object also has a static default user that fields from all documents can refer to.
UserInformation::get_DefaultUser()->set_Name(u"Default User");
UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"FieldOptions.CurrentUser.docx");
```

## See Also

* Class [UserInformation](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
