---
title: Aspose::Words::Fields::FieldUserAddress::set_UserAddress method
linktitle: set_UserAddress
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldUserAddress::set_UserAddress method. Sets the current user''s postal address in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fields/fielduseraddress/set_useraddress/
---
## FieldUserAddress::set_UserAddress method


Sets the current user's postal address.

```cpp
void Aspose::Words::Fields::FieldUserAddress::set_UserAddress(const System::String & value)
```

## Examples


Shows how to use the USERADDRESS field.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Create a UserInformation object and set it as the source of user information for any fields that we create.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Create a USERADDRESS field to display the current user's address,
// taken from the UserInformation object we created above.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<Aspose::Words::Fields::FieldUserAddress>(builder->InsertField(FieldType::FieldUserAddress, true));

ASSERT_EQ(u" USERADDRESS ", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"123 Main Street", fieldUserAddress->get_Result());

// We can set this property to get our field to override the value currently stored in the UserInformation object.
fieldUserAddress->set_UserAddress(u"456 North Road");
fieldUserAddress->Update();

ASSERT_EQ(u" USERADDRESS  \"456 North Road\"", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"456 North Road", fieldUserAddress->get_Result());

// This does not affect the value in the UserInformation object.
ASSERT_EQ(u"123 Main Street", doc->get_FieldOptions()->get_CurrentUser()->get_Address());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERADDRESS.docx");
```
## See Also

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
