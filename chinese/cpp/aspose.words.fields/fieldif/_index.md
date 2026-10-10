---
title: "Aspose::Words::Fields::FieldIf 类"
linktitle: "FieldIf"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIf 类。实现 IF 字段。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 54000
url: /zh/cpp/aspose.words.fields/fieldif/
---
## FieldIf class


实现 IF 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldIf : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IMergeFieldSurrogate
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [EvaluateCondition](./evaluatecondition/)() | 评估条件。 |
| [get_ComparisonOperator](./get_comparisonoperator/)() | 获取或设置比较运算符。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](./get_end/)() override | 获取表示字段结束的节点。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FalseText](./get_falsetext/)() | 获取或设置当比较表达式为 **false** 时显示的文本。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LeftExpression](./get_leftexpression/)() | 获取或设置比较表达式的左侧部分。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_RightExpression](./get_rightexpression/)() | 获取或设置比较表达式的右侧部分。 |
| [get_Separator](./get_separator/)() override | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](./get_start/)() override | 获取表示字段起始的节点。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| [get_TrueText](./get_truetext/)() | 获取或设置当比较表达式为 true 时显示的文本。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_ComparisonOperator](./set_comparisonoperator/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldIf::get_ComparisonOperator](./get_comparisonoperator/)。 |
| [set_FalseText](./set_falsetext/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldIf::get_FalseText](./get_falsetext/)。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LeftExpression](./set_leftexpression/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldIf::get_LeftExpression](./get_leftexpression/)。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_RightExpression](./set_rightexpression/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldIf::get_RightExpression](./get_rightexpression/)。 |
| [set_TrueText](./set_truetext/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldIf::get_TrueText](./get_truetext/)。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 备注


比较由表达式 [LeftExpression](./get_leftexpression/) 和 [RightExpression](./get_rightexpression/) 指定的值，使用由 [ComparisonOperator](./get_comparisonoperator/) 指定的运算符进行比较。

以下格式的字段将用作邮件合并源： { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
