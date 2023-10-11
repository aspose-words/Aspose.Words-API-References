---
title: FieldArgumentBuilder.AddText
second_title: Aspose.Words for .NET API 参考
description: FieldArgumentBuilder 方法. 将纯文本添加到参数中
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldargumentbuilder/addtext/
---
## FieldArgumentBuilder.AddText method

将纯文本添加到参数中。

```csharp
public FieldArgumentBuilder AddText(string text)
```

### 例子

演示如何使用字段生成器构造字段，然后将它们插入到文档中。

```csharp
Document doc = new Document();

// 下面是使用字段构建器完成字段构建的三个示例。
// 1 - 单个字段：
// 使用字段生成器添加显示 f（弗罗林）符号的 SYMBOL 字段。
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - 嵌套字段：
// 使用字段构建器创建由另一个字段构建器用作内部字段的公式字段。
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// 为另一个 SYMBOL 字段创建另一个构建器，并插入公式字段
// 我们在上面创建的 SYMBOL 字段中作为其参数。
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// 外部 SYMBOL 字段将使用公式字段结果 174 作为其参数，
// 这将使该字段显示 ®（注册符号）符号，因为其字符编号为 174。
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - 多个嵌套字段和参数：
// 现在，我们将使用构建器创建一个 IF 字段，该字段显示两个自定义字符串值之一，
// 取决于其表达式的真/假值。获取真/假值
// 确定 IF 字段显示哪个字符串，IF 字段将测试两个数字表达式是否相等。
// 我们将以公式字段的形式提供两个表达式，并将其嵌套在 IF 字段内。
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// 接下来，我们将构建两个字段参数，它们将用作 IF 字段的 true/false 输出字符串。
// 这些参数将重用我们的数值表达式的输出值。
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // 最后，我们将为 IF 字段再创建一个字段构建器并组合所有表达式。
builder = new FieldBuilder(FieldType.FieldIf);
builder.AddArgument(leftExpression);
builder.AddArgument("=");
builder.AddArgument(rightExpression);
builder.AddArgument(trueOutput);
builder.AddArgument(falseOutput);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

Assert.AreEqual(" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 " +
                "\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " +
                "\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### 也可以看看

* class [FieldArgumentBuilder](../)
* 命名空间 [Aspose.Words.Fields](../../fieldargumentbuilder/)
* 部件 [Aspose.Words](../../../)


