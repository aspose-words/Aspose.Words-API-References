---
title: FieldOptions.ComparisonExpressionEvaluator
second_title: Aspose.Words för .NET API Referens
description: FieldOptions fast egendom. Hämtar eller ställer in utvärderaren för fältjämförelseuttryck.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldoptions/comparisonexpressionevaluator/
---
## FieldOptions.ComparisonExpressionEvaluator property

Hämtar eller ställer in utvärderaren för fältjämförelseuttryck.

```csharp
public IComparisonExpressionEvaluator ComparisonExpressionEvaluator { get; set; }
```

### Exempel

Visar hur man implementerar anpassad utvärdering för IF- och COMPARE-fälten.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // Fältkoder som vi använder i detta exempel:
    // 1. " IF {0} {1} {2} \"true argument\" \"false argument\" ".
    // 2. " JÄMFÖR {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Om "comparisonResult" är odefinierat skapar vi "ComparisonEvaluationResult" med sträng, istället för bool.
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

* interface [IComparisonExpressionEvaluator](../../icomparisonexpressionevaluator/)
* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../fieldoptions/)
* hopsättning [Aspose.Words](../../../)


