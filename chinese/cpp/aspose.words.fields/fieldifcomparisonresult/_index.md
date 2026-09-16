---
title: "Aspose::Words::Fields::FieldIfComparisonResult 枚举"
linktitle: "FieldIfComparisonResult"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIfComparisonResult 枚举。指定 IF 字段条件评估的结果（C++）。"
type: docs
weight: 128000
url: /zh/cpp/aspose.words.fields/fieldifcomparisonresult/
---
## FieldIfComparisonResult enum


指定 IF 字段条件求值的结果。

```cpp
enum class FieldIfComparisonResult
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 错误 | 0 | 条件中存在错误。 |
| True | 1 | 条件为 **true**。 |
| False | 2 | 条件为 **false**。 |


## 示例



展示如何插入 IF 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// IF 字段将显示来自其 "TrueText" 属性的字符串，
// 或其 "FalseText" 属性，取决于我们构造的语句的真值。
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// 在此情况下，"0 = 1" 不正确，因此显示的结果将是 "False"。
ASSERT_EQ(u" IF  0 = 1 True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::False, field->EvaluateCondition());
ASSERT_EQ(u"False", field->get_Result());

builder->Write(u"\nStatement 2: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// 这次语句是正确的，因此显示的结果将是 "True"。
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
