---
title: ComparisonEvaluationResult
second_title: Aspose.Words per .NET API Reference
description: Crea un risultato di valutazione del confronto.
type: docs
weight: 10
url: /it/net/aspose.words.fields/comparisonevaluationresult/comparisonevaluationresult/
---
## ComparisonEvaluationResult(bool) {#constructor}

Crea un risultato di valutazione del confronto.

```csharp
public ComparisonEvaluationResult(bool result)
```

### Esempi

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
    // 1. " IF {0} {1} {2} \"vero argomento\" \"falso argomento\" ".
    // 2. " CONFRONTA {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Se "comparisonResult" non è definito, creiamo "ComparisonEvaluationResult" con string, invece di bool.
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

* class [ComparisonEvaluationResult](../../comparisonevaluationresult)
* spazio dei nomi [Aspose.Words.Fields](../../comparisonevaluationresult)
* assemblea [Aspose.Words](../../../)

---

## ComparisonEvaluationResult(string) {#constructor_1}

Crea un risultato di valutazione del confronto non riuscito con il messaggio di errore corrispondente.

```csharp
public ComparisonEvaluationResult(string errorMessage)
```

### Esempi

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
    // 1. " IF {0} {1} {2} \"vero argomento\" \"falso argomento\" ".
    // 2. " CONFRONTA {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Se "comparisonResult" non è definito, creiamo "ComparisonEvaluationResult" con string, invece di bool.
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

* class [ComparisonEvaluationResult](../../comparisonevaluationresult)
* spazio dei nomi [Aspose.Words.Fields](../../comparisonevaluationresult)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
