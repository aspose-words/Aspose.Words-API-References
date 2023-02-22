---
title: ComparisonExpression.LeftExpression
second_title: Référence de l'API Aspose.Words pour .NET
description: ComparisonExpression propriété. Obtient lexpression de gauche.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/comparisonexpression/leftexpression/
---
## ComparisonExpression.LeftExpression property

Obtient l'expression de gauche.

```csharp
public string LeftExpression { get; }
```

### Exemples

Montre comment implémenter une évaluation personnalisée pour les champs IF et COMPARE.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // Codes de champ que nous utilisons dans cet exemple :
    // 1. " SI {0} {1} {2} \"vrai argument\" \"faux argument\" ".
    // 2. " COMPARER {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Si le "comparisonResult" n'est pas défini, nous créons "ComparisonEvaluationResult" avec une chaîne, au lieu de bool.
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
/// Évaluation des expressions de comparaison pour FieldIf et FieldCompare.
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

### Voir également

* class [ComparisonExpression](../)
* espace de noms [Aspose.Words.Fields](../../comparisonexpression/)
* Assemblée [Aspose.Words](../../../)


