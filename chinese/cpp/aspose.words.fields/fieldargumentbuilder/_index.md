---
title: "Aspose::Words::Fields::FieldArgumentBuilder class"
linktitle: "FieldArgumentBuilder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldArgumentBuilder 类。构建由字段、节点和纯文本组成的复杂字段参数。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.fields/fieldargumentbuilder/
---
## FieldArgumentBuilder class


构建由字段、节点和纯文本组成的复杂字段参数。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldArgumentBuilder : public Aspose::Words::Fields::IFieldBuildingBlock
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [AddField](./addfield/)(const System::SharedPtr\<Aspose::Words::Fields::FieldBuilder\>\&) | 向参数添加由 [FieldBuilder](../fieldbuilder/) 表示的字段。 |
| [AddNode](./addnode/)(const System::SharedPtr\<Aspose::Words::Inline\>\&) | 向参数添加一个节点。 |
| [AddText](./addtext/)(const System::String\&) | 向参数添加纯文本。 |
| [FieldArgumentBuilder](./fieldargumentbuilder/)() | 初始化 [FieldArgumentBuilder](./) 类的实例。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## 示例



展示如何使用字段构建器构建字段，然后将其插入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 以下是使用字段构建器进行字段构建的三个示例。
// 1 -  单字段：
// 使用字段构建器添加一个显示 ƒ（Florin）符号的 SYMBOL 字段。
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  嵌套字段：
// 使用字段构建器创建一个公式字段，该字段被另一个字段构建器用作内部字段。
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// 为另一个 SYMBOL 字段创建另一个构建器，并插入公式字段
// 我们上面创建的公式字段作为参数插入到该 SYMBOL 字段中。
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// 外部的 SYMBOL 字段将使用公式字段的结果 174 作为其参数，
// 由于字符编号为 174，这将使字段显示 ®（注册商标）符号。
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  多个嵌套字段和参数：
// 现在，我们将使用构建器创建一个 IF 字段，该字段显示两个自定义字符串值中的一个，
// 取决于其表达式的真/假值。要获取真/假值
// 该值决定 IF 字段显示哪个字符串，IF 字段将测试两个数值表达式是否相等。
// 我们将以公式字段的形式提供这两个表达式，并将它们嵌套在 IF 字段中。
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// 接下来，我们将构建两个字段参数，这些参数将作为 IF 字段的真/假输出字符串。
// 这些参数将复用我们数值表达式的输出值。
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// 最后，我们将为 IF 字段创建另一个字段构建器，并将所有表达式组合起来。
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldIf);
builder->AddArgument(leftExpression);
builder->AddArgument(u"=");
builder->AddArgument(rightExpression);
builder->AddArgument(trueOutput);
builder->AddArgument(falseOutput);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

ASSERT_EQ(System::String(u" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 ") + u"\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " + u"\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
