---
title: Aspose::Words::Fields::UserInformation class
linktitle: UserInformation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::UserInformation class. Specifies information about the user. To learn more, visit the  documentation article in C++.'
type: docs
weight: 117000
url: /cpp/aspose.words.fields/userinformation/
---
## UserInformation class


Specifies information about the user. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class UserInformation : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Address](./get_address/)() const | Gets or sets the user's postal address. |
| static [get_DefaultUser](./get_defaultuser/)() | Default user information. |
| [get_Initials](./get_initials/)() const | Gets or sets the user's initials. |
| [get_Name](./get_name/)() const | Gets or sets the user's name. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Address](./set_address/)(const System::String\&) | Setter for [Aspose::Words::Fields::UserInformation::get_Address](./get_address/). |
| [set_Initials](./set_initials/)(const System::String\&) | Setter for [Aspose::Words::Fields::UserInformation::get_Initials](./get_initials/). |
| [set_Name](./set_name/)(const System::String\&) | Setter for [Aspose::Words::Fields::UserInformation::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [UserInformation](./userinformation/)() |  |

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
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// The field options object also has a static default user that fields from all documents can refer to.
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

## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
