---
title: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials 方法"
linktitle: "get_UserInitials"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldUserInitials::get_UserInitials 方法。获取或设置当前用户的首字母缩写（在 C++ 中）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fielduserinitials/get_userinitials/
---
## FieldUserInitials::get_UserInitials method


获取或设置当前用户的首字母缩写。

```cpp
System::String Aspose::Words::Fields::FieldUserInitials::get_UserInitials()
```


## 示例



展示如何使用 USERINITIALS 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建一个 UserInformation 对象，并将其设置为我们创建的任何字段的用户信息来源。
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Initials(u"J. D.");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// 创建一个 USERINITIALS 字段以显示当前用户的首字母，
// 取自我们上面创建的 UserInformation 对象。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto fieldUserInitials = System::ExplicitCast<Aspose::Words::Fields::FieldUserInitials>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldUserInitials, true));
ASSERT_EQ(userInformation->get_Initials(), fieldUserInitials->get_Result());

ASSERT_EQ(u" USERINITIALS ", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. D.", fieldUserInitials->get_Result());

// 我们可以设置此属性，使我们的字段覆盖当前存储在 UserInformation 对象中的值。
fieldUserInitials->set_UserInitials(u"J. C.");
fieldUserInitials->Update();

ASSERT_EQ(u" USERINITIALS  \"J. C.\"", fieldUserInitials->GetFieldCode());
ASSERT_EQ(u"J. C.", fieldUserInitials->get_Result());

// 这不会影响 UserInformation 对象中的值。
ASSERT_EQ(u"J. D.", doc->get_FieldOptions()->get_CurrentUser()->get_Initials());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.USERINITIALS.docx");
```

## 另见

* Class [FieldUserInitials](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
