---
title: "Aspose::Words::Fields::FieldUserName::get_UserName 方法"
linktitle: "get_UserName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldUserName::get_UserName 方法。获取或设置当前用户的名称（在 C++ 中）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldusername/get_username/
---
## FieldUserName::get_UserName method


获取或设置当前用户的名称。

```cpp
System::String Aspose::Words::Fields::FieldUserName::get_UserName()
```


## 示例



展示如何使用 USERNAME 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建一个 UserInformation 对象，并将其设置为我们创建的任何字段的用户信息来源。
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个 USERNAME 字段以显示当前用户的名称，
// 取自我们上面创建的 UserInformation 对象。
auto fieldUserName = System::ExplicitCast<Aspose::Words::Fields::FieldUserName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserName, true));
ASSERT_EQ(userInformation->get_Name(), fieldUserName->get_Result());

ASSERT_EQ(u" USERNAME ", fieldUserName->GetFieldCode());
ASSERT_EQ(u"John Doe", fieldUserName->get_Result());

// 我们可以设置此属性，使我们的字段覆盖当前存储在 UserInformation 对象中的值。
fieldUserName->set_UserName(u"Jane Doe");
fieldUserName->Update();

ASSERT_EQ(u" USERNAME  \"Jane Doe\"", fieldUserName->GetFieldCode());
ASSERT_EQ(u"Jane Doe", fieldUserName->get_Result());

// 这不会影响 UserInformation 对象中的值。
ASSERT_EQ(u"John Doe", doc->get_FieldOptions()->get_CurrentUser()->get_Name());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERNAME.docx");
```

## 另见

* Class [FieldUserName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
