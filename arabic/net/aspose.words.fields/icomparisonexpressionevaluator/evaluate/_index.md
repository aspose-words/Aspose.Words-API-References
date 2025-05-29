---
title: IComparisonExpressionEvaluator.Evaluate
linktitle: Evaluate
articleTitle: Evaluate
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة التقييم في IComparisonExpressionEvaluator لإجراء تقييمات مقارنة دقيقة. حسّن كفاءة ترميزك باستخدام أداتنا الفعّالة!
type: docs
weight: 10
url: /ar/net/aspose.words.fields/icomparisonexpressionevaluator/evaluate/
---
## IComparisonExpressionEvaluator.Evaluate method

يقوم بتقييم تعبير المقارنة.

```csharp
public ComparisonEvaluationResult Evaluate(Field field, ComparisonExpression expression)
```

## ملاحظات

يجب أن يعود التنفيذ`باطل` للإشارة إلى أنه يجب إجراء التقييم الافتراضي.

## أمثلة

يوضح كيفية تنفيذ التقييم المخصص لحقول IF و COMPARE.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // رموز الحقول التي نستخدمها في هذا المثال:
    // 1. "إذا {0} {1} {2} \"حجة صحيحة\" \"حجة خاطئة\" ".
    // 2. " قارن {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // إذا كانت "comparisonResult" غير محددة، نقوم بإنشاء "ComparisonEvaluationResult" بسلسلة، بدلاً من bool.
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
/// تقييم تعبيرات المقارنة لـ FieldIf وFieldCompare.
/// </summary>
private class ComparisonExpressionEvaluator : IComparisonExpressionEvaluator
{
    public ComparisonExpressionEvaluator(ComparisonEvaluationResult result)
    {
        mResult = result;
        if (mResult != null)
        {
            Console.WriteLine(mResult.ErrorMessage);
            Console.WriteLine(mResult.Result);
        }
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

* class [ComparisonEvaluationResult](../../comparisonevaluationresult/)
* class [Field](../../field/)
* class [ComparisonExpression](../../comparisonexpression/)
* interface [IComparisonExpressionEvaluator](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
