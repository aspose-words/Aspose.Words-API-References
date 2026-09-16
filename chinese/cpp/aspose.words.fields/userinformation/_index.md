---
title: "Aspose::Words::Fields::UserInformation class"
linktitle: "UserInformation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::UserInformation class. 指定有关用户的信息。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 117000
url: /zh/cpp/aspose.words.fields/userinformation/
---
## UserInformation class


指定有关用户的信息。要了解更多信息，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class UserInformation : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Address](./get_address/)() const | 获取或设置用户的邮政地址。 |
| static [get_DefaultUser](./get_defaultuser/)() | 默认用户信息。 |
| [get_Initials](./get_initials/)() const | 获取或设置用户的缩写。 |
| [get_Name](./get_name/)() const | 获取或设置用户的姓名。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Address](./set_address/)(const System::String\&) | 用于 [Aspose::Words::Fields::UserInformation::get_Address](./get_address/) 的设置器。 |
| [set_Initials](./set_initials/)(const System::String\&) | 用于 [Aspose::Words::Fields::UserInformation::get_Initials](./get_initials/) 的设置器。 |
| [set_Name](./set_name/)(const System::String\&) | 用于 [Aspose::Words::Fields::UserInformation::get_Name](./get_name/) 的设置器。 |
| static [Type](./type/)() |  |
| [UserInformation](./userinformation/)() |  |

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
