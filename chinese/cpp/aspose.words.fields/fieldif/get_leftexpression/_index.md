---
title: "Aspose::Words::Fields::FieldIf::get_LeftExpression 方法"
linktitle: "get_LeftExpression"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIf::get_LeftExpression 方法。获取或设置比较表达式的左侧部分（C++）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.fields/fieldif/get_leftexpression/
---
## FieldIf::get_LeftExpression method


获取或设置比较表达式的左侧部分。

```cpp
System::String Aspose::Words::Fields::FieldIf::get_LeftExpression()
```


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

* Class [FieldIf](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
