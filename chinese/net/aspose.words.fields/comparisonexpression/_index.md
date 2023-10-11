---
title: Class ComparisonExpression
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.ComparisonExpression 班级. 比较表达式.
type: docs
weight: 1490
url: /zh/net/aspose.words.fields/comparisonexpression/
---
## ComparisonExpression class

比较表达式.

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public sealed class ComparisonExpression
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/comparisonexpression/comparisonoperator/) { get; } | 获取比较运算符。 |
| [LeftExpression](../../aspose.words.fields/comparisonexpression/leftexpression/) { get; } | 获取左侧表达式。 |
| [RightExpression](../../aspose.words.fields/comparisonexpression/rightexpression/) { get; } | 获得正确的表达式。 |

### 例子

展示如何实现 IF 和 COMPARE 字段的自定义评估。

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // 我们在此示例中使用的字段代码：
    // 1." IF {0} {1} {2} \"真参数\" \"假参数\" "。
    // 2.“比较{0} {1} {2}”。
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // 如果“comparisonResult”未定义，我们使用字符串而不是布尔值创建“ComparisonEvaluationResult”。
    ComparisonEvaluationResult result = comparisonResult != -1
        ? new ComparisonEvaluationResult(comparisonResult == 1)
        : comparisonError != null ? new ComparisonEvaluationResult(comparisonError) : null;

    ComparisonExpressionEvaluator evaluator = new ComparisonExpressionEvaluator(result);
    builder.Document.FieldOptions.ComparisonExpressionEvaluator = evaluator;

    builder.Document.UpdateFields();

    Assert.AreEqual(expectedResult, field.Result);
    evaluator.AssertInvocationsCount(1).AssertInvocationArguments(0, left, @operator, right);
}

/// <summary>
/// FieldIf 和 FieldCompare 的比较表达式评估。
/// </summary>
private class ComparisonExpressionEvaluator : IComparisonExpressionEvaluator
{
    public ComparisonExpressionEvaluator(ComparisonEvaluationResult result)
    {
        mResult = result;
    }

    public ComparisonEvaluationResult Evaluate(Field field, ComparisonExpression expression)
    {
        mInvocations.Add(new[]
        {
            expression.LeftExpression,
            expression.ComparisonOperator,
            expression.RightExpression
        });

        return mResult;
    }

    public ComparisonExpressionEvaluator AssertInvocationsCount(int expected)
    {
        Assert.AreEqual(expected, mInvocations.Count);
        return this;
    }

    public ComparisonExpressionEvaluator AssertInvocationArguments(
        int invocationIndex,
        string expectedLeftExpression,
        string expectedComparisonOperator,
        string expectedRightExpression)
    {
        string[] arguments = mInvocations[invocationIndex];

        Assert.AreEqual(expectedLeftExpression, arguments[0]);
        Assert.AreEqual(expectedComparisonOperator, arguments[1]);
        Assert.AreEqual(expectedRightExpression, arguments[2]);

        return this;
    }

    private readonly ComparisonEvaluationResult mResult;
    private readonly List<string[]> mInvocations = new List<string[]>();
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


