---
title: "Aspose::Words::Fields::FormField::get_Type 方法"
linktitle: "get_Type"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FormField::get_Type 方法。返回 C++ 中的表单字段类型。"
type: docs
weight: 24000
url: /zh/cpp/aspose.words.fields/formfield/get_type/
---
## FormField::get_Type method


返回表单字段的类型。

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FormField::get_Type()
```


## 示例



展示如何插入组合框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// 插入一个组合框，允许用户从字符串集合中选择一个选项。
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// 表单字段将以 "select" HTML 标签的形式出现。
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## 另见

* Enum [FieldType](../../fieldtype/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
