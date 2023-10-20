---
title: ComparisonEvaluationResult Class
linktitle: ComparisonEvaluationResult
articleTitle: ComparisonEvaluationResult
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.ComparisonEvaluationResult 班级. 比较评估结果 在 C#.
type: docs
weight: 1480
url: /zh/net/aspose.words.fields/comparisonevaluationresult/
---
## ComparisonEvaluationResult class

比较评估结果。

```csharp
public sealed class ComparisonEvaluationResult
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ComparisonEvaluationResult](comparisonevaluationresult/#constructor)(*bool*) | 创建比较评估结果。 |
| [ComparisonEvaluationResult](comparisonevaluationresult/#constructor_1)(*string*) | 使用相应的错误消息创建失败的比较评估结果。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ErrorMessage](../../aspose.words.fields/comparisonevaluationresult/errormessage/) { get; } | 获取比对评估结果失败的错误信息。 |
| [Result](../../aspose.words.fields/comparisonevaluationresult/result/) { get; } | 获取比较评估结果。 |

## 例子

显示如何为 IF 和 COMPARE 字段实施自定义评估。

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // 我们在此示例中使用的字段代码：
    // 1. " IF {0} {1} {2} \"真参数\" \"假参数\" "。
    // 2.“比较 {0} {1} {2}”。
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // 如果 "comparisonResult" 未定义，我们用字符串而不是 bool 创建 "ComparisonEvaluationResult"。
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
/// FieldIf 和 FieldCompare 的比较表达式计算。
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
