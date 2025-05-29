---
title: IComparisonExpressionEvaluator Interface
linktitle: IComparisonExpressionEvaluator
articleTitle: IComparisonExpressionEvaluator
second_title: Aspose.Words för .NET
description: Förbättra din dokumenthantering med Aspose.Words.Fields.IComparisonExpressionEvaluator. Anpassa jämförelseutvärderingar för FieldIf- och FieldCompare-fälten utan ansträngning!
type: docs
weight: 3090
url: /sv/net/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface

När den är implementerad, tillåter den att åsidosätta standardutvärderingen av jämförelseuttryck för[`FieldIf`](../fieldif/) och[`FieldCompare`](../fieldcompare/) fält.

```csharp
public interface IComparisonExpressionEvaluator
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Evaluate](../../aspose.words.fields/icomparisonexpressionevaluator/evaluate/)(*[Field](../field/), [ComparisonExpression](../comparisonexpression/)*) | Utvärderar jämförelseuttryck. |

## Exempel

Visar hur man implementerar anpassad utvärdering för fälten OM och JÄMFÖR.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // Fältkoder som vi använder i det här exemplet:
    // 1. " OM {0} {1} {2} "sant argument" "falskt argument" .
    // 2. "JÄMFÖR {0} {1} {2}".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Om "comparisonResult" är odefinierat skapar vi "ComparisonEvaluationResult" med strängen istället för bool.
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
/// Utvärdering av jämförelseuttryck för FieldIf och FieldCompare.
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

### Se även

* property [ComparisonExpressionEvaluator](../fieldoptions/comparisonexpressionevaluator/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
