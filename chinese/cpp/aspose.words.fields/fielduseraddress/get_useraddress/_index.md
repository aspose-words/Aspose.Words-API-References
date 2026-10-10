---
title: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress 方法"
linktitle: "get_UserAddress"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldUserAddress::get_UserAddress 方法。获取或设置当前用户的邮政地址（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fielduseraddress/get_useraddress/
---
## FieldUserAddress::get_UserAddress method


获取或设置当前用户的邮政地址。

```cpp
System::String Aspose::Words::Fields::FieldUserAddress::get_UserAddress()
```


## 示例



展示如何使用 USERADDRESS 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建一个 UserInformation 对象，并将其设置为我们创建的任何字段的用户信息来源。
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// 创建 USERADDRESS 字段以显示当前用户的地址，
// 取自我们上面创建的 UserInformation 对象。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserAddress = System::ExplicitCast<Aspose::Words::Fields::FieldUserAddress>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserAddress, true));

ASSERT_EQ(u" USERADDRESS ", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"123 Main Street", fieldUserAddress->get_Result());

// 我们可以设置此属性，使我们的字段覆盖当前存储在 UserInformation 对象中的值。
fieldUserAddress->set_UserAddress(u"456 North Road");
fieldUserAddress->Update();

ASSERT_EQ(u" USERADDRESS  \"456 North Road\"", fieldUserAddress->GetFieldCode());
ASSERT_EQ(u"456 North Road", fieldUserAddress->get_Result());

// 这不会影响 UserInformation 对象中的值。
ASSERT_EQ(u"123 Main Street", doc->get_FieldOptions()->get_CurrentUser()->get_Address());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERADDRESS.docx");
```

## 另见

* Class [FieldUserAddress](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
