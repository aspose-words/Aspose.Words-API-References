---
title: IComparisonExpressionEvaluator.Evaluate
linktitle: Evaluate
articleTitle: Evaluate
second_title: Aspose.Words für .NET
description: Entdecken Sie die Evaluate-Methode des IComparisonExpressionEvaluators für präzise Vergleichsauswertungen. Steigern Sie Ihre Programmiereffizienz mit unserem leistungsstarken Tool!
type: docs
weight: 10
url: /de/net/aspose.words.fields/icomparisonexpressionevaluator/evaluate/
---
## IComparisonExpressionEvaluator.Evaluate method

Wertet den Vergleichsausdruck aus.

```csharp
public ComparisonEvaluationResult Evaluate(Field field, ComparisonExpression expression)
```

## Bemerkungen

Die Implementierung sollte zurückgeben`null` um anzugeben, dass die Standardauswertung durchgeführt werden soll.

## Beispiele

Zeigt, wie eine benutzerdefinierte Auswertung für die Felder „WENN“ und „VERGLEICHEN“ implementiert wird.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // Feldcodes, die wir in diesem Beispiel verwenden:
    // 1. " WENN {0} {1} {2} \"wahres Argument\" \"falsches Argument\" ".
    // 2. " VERGLEICHEN SIE {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Wenn „comparisonResult“ nicht definiert ist, erstellen wir „ComparisonEvaluationResult“ mit einem String statt mit einem booleschen Wert.
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
/// Auswertung der Vergleichsausdrücke für FieldIf und FieldCompare.
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

### Siehe auch

* class [ComparisonEvaluationResult](../../comparisonevaluationresult/)
* class [Field](../../field/)
* class [ComparisonExpression](../../comparisonexpression/)
* interface [IComparisonExpressionEvaluator](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
