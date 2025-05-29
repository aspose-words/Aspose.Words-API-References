---
title: ComparisonEvaluationResult Class
linktitle: ComparisonEvaluationResult
articleTitle: ComparisonEvaluationResult
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.ComparisonEvaluationResult för effektiv dokumentjämförelseanalys. Få insikter och förbättra ditt arbetsflöde!
type: docs
weight: 1890
url: /sv/net/aspose.words.fields/comparisonevaluationresult/
---
## ComparisonEvaluationResult class

Resultatet av jämförelseutvärderingen.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public sealed class ComparisonEvaluationResult
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ComparisonEvaluationResult](comparisonevaluationresult/#constructor)(*bool*) | Skapar ett jämförande utvärderingsresultat. |
| [ComparisonEvaluationResult](comparisonevaluationresult/#constructor_1)(*string*) | Skapar ett misslyckat jämförelseutvärderingsresultat med motsvarande felmeddelande. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ErrorMessage](../../aspose.words.fields/comparisonevaluationresult/errormessage/) { get; } | Hämtar felmeddelandet för det misslyckade jämförelseutvärderingsresultatet. |
| [Result](../../aspose.words.fields/comparisonevaluationresult/result/) { get; } | Hämtar resultatet av jämförelseutvärderingen. |

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

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
