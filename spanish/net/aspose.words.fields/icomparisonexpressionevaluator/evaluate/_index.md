---
title: IComparisonExpressionEvaluator.Evaluate
linktitle: Evaluate
articleTitle: Evaluate
second_title: Aspose.Words para .NET
description: Descubra el método Evaluate de IComparisonExpressionEvaluator para realizar evaluaciones comparativas precisas. ¡Mejore su eficiencia de codificación con nuestra potente herramienta!
type: docs
weight: 10
url: /es/net/aspose.words.fields/icomparisonexpressionevaluator/evaluate/
---
## IComparisonExpressionEvaluator.Evaluate method

Evalúa la expresión de comparación.

```csharp
public ComparisonEvaluationResult Evaluate(Field field, ComparisonExpression expression)
```

## Observaciones

La implementación debería retornar`nulo` para indicar que se debe realizar la evaluación predeterminada.

## Ejemplos

Muestra cómo implementar la evaluación personalizada para los campos SI y COMPARAR.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // Códigos de campo que utilizamos en este ejemplo:
    // 1. " SI {0} {1} {2} \"argumento verdadero\" \"argumento falso\" ".
    // 2. " COMPARAR {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Si "comparisonResult" no está definido, creamos "ComparisonEvaluationResult" con una cadena, en lugar de un valor booleano.
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
/// Evaluación de expresiones de comparación para FieldIf y FieldCompare.
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

### Ver también

* class [ComparisonEvaluationResult](../../comparisonevaluationresult/)
* class [Field](../../field/)
* class [ComparisonExpression](../../comparisonexpression/)
* interface [IComparisonExpressionEvaluator](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
