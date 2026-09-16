---
title: "Aspose::Words::Fields::FieldOptions::get_CurrentUser 方法"
linktitle: "get_CurrentUser"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldOptions::get_CurrentUser 方法。获取或设置 C++ 中的当前用户信息。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.fields/fieldoptions/get_currentuser/
---
## FieldOptions::get_CurrentUser method


获取或设置当前用户信息。

```cpp
const System::SharedPtr<Aspose::Words::Fields::UserInformation> & Aspose::Words::Fields::FieldOptions::get_CurrentUser() const
```


## 示例



展示如何设置用户详细信息，并使用字段显示它们。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 UserInformation 对象，并将其设置为显示用户信息的字段的数据源。
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// 插入 USERNAME、USERINITIALS 和 USERADDRESS 字段，这些字段显示
// 我们上面创建的 UserInformation 对象的相应属性。
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// 字段选项对象还具有一个静态默认用户，所有文档中的字段都可以引用它。
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

## 另见

* Class [UserInformation](../../userinformation/)
* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
