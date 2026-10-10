---
title: "Aspose::Words::Fields::FieldCompare::get_LeftExpression 方法"
linktitle: "get_LeftExpression"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldCompare::get_LeftExpression 方法。获取或设置 C++ 中比较表达式的左侧部分。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fields/fieldcompare/get_leftexpression/
---
## FieldCompare::get_LeftExpression method


获取或设置比较表达式的左侧部分。

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_LeftExpression()
```


## 示例



展示如何使用 COMPARE 字段比较表达式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// COMPARE 字段显示 "0" 或 "1"，取决于其语句的真假。
// 此语句的结果为 false，因此该字段将显示 "0"。
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// 由于语句为 true，此字段显示 "1"。
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.COMPARE.docx");
```

## 另见

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
