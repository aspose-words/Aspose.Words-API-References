---
title: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat 方法"
linktitle: "get_LegacyNumberFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat 方法。获取或设置指示在 C++ 中是否启用字段的传统（早于 AW 13.10）数字格式的值。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.fields/fieldoptions/get_legacynumberformat/
---
## FieldOptions::get_LegacyNumberFormat method


获取或设置指示是否启用旧版（早于 AW 13.10）字段数字格式的值。

```cpp
bool Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat() const
```

## 备注


当此属性设置为 **true** 时，模板符号 \"#\" 的行为与 .net 中相同：如果存在相应的数字，则用该数字替换井号；否则，结果字符串中不出现任何符号。

当此属性设置为 **false** 时，模板符号 \"#\" 的行为与 MS Word 相同：此格式项指定结果中要显示的必需数字位数。如果结果在该位置没有数字，MS Word 会显示空格。例如，{ = 9 + 6 \\# $### } 显示 $ 15。

默认值为 **false**。

## 示例



展示如何为字段启用传统数字格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3 \\# $##");

ASSERT_EQ(u"$ 5", field->get_Result());

doc->get_FieldOptions()->set_LegacyNumberFormat(true);
field->Update();

ASSERT_EQ(u"$5", field->get_Result());
```

## 另见

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
