---
title: IComparisonExpressionEvaluator Interface
linktitle: IComparisonExpressionEvaluator
articleTitle: IComparisonExpressionEvaluator
second_title: Aspose.Words لـ .NET
description: حسّن معالجة مستنداتك باستخدام Aspose.Words.Fields.IComparisonExpressionEvaluator. خصّص تقييمات المقارنة لحقول FieldIf وFieldCompare بسهولة!
type: docs
weight: 3090
url: /ar/net/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface

عند تنفيذه، يسمح بتجاوز تقييم تعبيرات المقارنة الافتراضية لـ[`FieldIf`](../fieldif/) و[`FieldCompare`](../fieldcompare/) الحقول.

```csharp
public interface IComparisonExpressionEvaluator
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Evaluate](../../aspose.words.fields/icomparisonexpressionevaluator/evaluate/)(*[Field](../field/), [ComparisonExpression](../comparisonexpression/)*) | يقوم بتقييم تعبير المقارنة. |

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

* property [ComparisonExpressionEvaluator](../fieldoptions/comparisonexpressionevaluator/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
