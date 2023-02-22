---
title: Class ComparisonExpression
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.ComparisonExpression فصل. تعبير المقارنة .
type: docs
weight: 1340
url: /ar/net/aspose.words.fields/comparisonexpression/
---
## ComparisonExpression class

تعبير المقارنة .

```csharp
public sealed class ComparisonExpression
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/comparisonexpression/comparisonoperator/) { get; } | يحصل على عامل المقارنة . |
| [LeftExpression](../../aspose.words.fields/comparisonexpression/leftexpression/) { get; } | يحصل على التعبير الأيسر . |
| [RightExpression](../../aspose.words.fields/comparisonexpression/rightexpression/) { get; } | الحصول على التعبير الصحيح . |

### أمثلة

يوضح كيفية تنفيذ التقييم المخصص لحقلي IF و COMPARE.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // أكواد الحقول التي نستخدمها في هذا المثال:
    // 1. "إذا {0} {1} {2} \" وسيطة صحيحة \ "\" وسيطة خاطئة \ "".
    // 2. "قارن {0} {1} {2}".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // إذا كانت "ComparisonEvaluationResult" غير محددة ، فإننا ننشئ "ComparisonEvaluationResult" بسلسلة بدلاً من منطقي.
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
/// تقييم تعبيرات المقارنة لـ FieldIf و FieldCompare.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


