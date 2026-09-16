---
title: "Aspose::Words::Fields::FormField::get_Result 方法"
linktitle: "get_Result"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FormField::get_Result 方法。获取或设置表示此表单字段结果的字符串（C++）。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words.fields/formfield/get_result/
---
## FormField::get_Result method


获取或设置表示此表单字段结果的字符串。

```cpp
System::String Aspose::Words::Fields::FormField::get_Result()
```

## 备注


对于文本表单字段，结果是字段中的文本。

对于复选框表单字段，结果可以是 "1" 或 "0"，用于表示已选或未选。

对于下拉列表表单字段，结果是下拉列表中选中的字符串。

为文本表单字段设置 [Result](./) 不会应用在 [TextInputFormat](../get_textinputformat/) 中指定的文本格式。如果想设置值并应用格式，请使用 [SetTextInputValue()](../) 方法。

对于文本表单字段，如果 *value* 为 **null**，则会应用 [TextInputDefault](../get_textinputdefault/) 的值。

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

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
