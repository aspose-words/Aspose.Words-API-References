---
title: Aspose::Words::Fields::FieldUserAddress::get_UserAddress method
linktitle: get_UserAddress
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldUserAddress::get_UserAddress method. Gets or sets the current user''s postal address in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fielduseraddress/get_useraddress/
---
## FieldUserAddress::get_UserAddress method


Gets or sets the current user's postal address.

```cpp
System::String Aspose::Words::Fields::FieldUserAddress::get_UserAddress()
```


## Examples



Shows how to use the USERADDRESS field. 
```cpp
auto doc = MakeObject<Document>();

// Create a UserInformation object and set it as the source of user information for any fields that we create.
auto userInformation = MakeObject<UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Create a USERADDRESS field to display the current user's address,
// taken from the UserInformation object we created above.
auto builder = MakeObject<DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<FieldUserAddress>(builder->InsertField(FieldType::FieldUserAddress, true));

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
doc->Save(ArtifactsDir + u"Field.USERADDRESS.docx");
```

## See Also

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
