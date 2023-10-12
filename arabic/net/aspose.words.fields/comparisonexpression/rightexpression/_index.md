---
title: ComparisonExpression.RightExpression
second_title: Aspose.Words لمراجع .NET API
description: ComparisonExpression ملكية. الحصول على التعبير الصحيح.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/comparisonexpression/rightexpression/
---
## ComparisonExpression.RightExpression property

الحصول على التعبير الصحيح.

```csharp
public string RightExpression { get; }
```

### أمثلة

يوضح كيفية تنفيذ التقييم المخصص لحقول IF وCOMPARE.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // رموز الحقول التي نستخدمها في هذا المثال:
    // 1. " IF {0} {1} {2} \"الوسيطة الحقيقية\" \"الوسيطة الخاطئة\" ".
    // 2. " قارن {0} {1} {2}".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // إذا كانت "comparisonResult" غير محددة، فإننا ننشئ "ComparisonEvaluationResult" بسلسلة بدلاً من bool.
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

* class [ComparisonExpression](../)
* مساحة الاسم [Aspose.Words.Fields](../../comparisonexpression/)
* المجسم [Aspose.Words](../../../)


