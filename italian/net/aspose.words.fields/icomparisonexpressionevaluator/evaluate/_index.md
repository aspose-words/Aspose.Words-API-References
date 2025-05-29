---
title: IComparisonExpressionEvaluator.Evaluate
linktitle: Evaluate
articleTitle: Evaluate
second_title: Aspose.Words per .NET
description: Scopri il metodo Evaluate di IComparisonExpressionEvaluator per valutazioni comparative precise. Migliora la tua efficienza di programmazione con il nostro potente strumento!
type: docs
weight: 10
url: /it/net/aspose.words.fields/icomparisonexpressionevaluator/evaluate/
---
## IComparisonExpressionEvaluator.Evaluate method

Valuta l'espressione di confronto.

```csharp
public ComparisonEvaluationResult Evaluate(Field field, ComparisonExpression expression)
```

## Osservazioni

L'implementazione dovrebbe restituire`null` per indicare che deve essere eseguita la valutazione predefinita.

## Esempi

Mostra come implementare la valutazione personalizzata per i campi SE e CONFRONTA.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // Codici di campo che utilizziamo in questo esempio:
    // 1. " SE {0} {1} {2} \"argomento vero\" \"argomento falso\" ".
    // 2. "CONFRONTA {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Se "comparisonResult" non è definito, creiamo "ComparisonEvaluationResult" con stringa, anziché bool.
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
/// Valutazione delle espressioni di confronto per FieldIf e FieldCompare.
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

### Guarda anche

* class [ComparisonEvaluationResult](../../comparisonevaluationresult/)
* class [Field](../../field/)
* class [ComparisonExpression](../../comparisonexpression/)
* interface [IComparisonExpressionEvaluator](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
