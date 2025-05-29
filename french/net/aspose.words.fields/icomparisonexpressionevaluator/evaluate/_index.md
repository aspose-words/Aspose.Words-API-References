---
title: IComparisonExpressionEvaluator.Evaluate
linktitle: Evaluate
articleTitle: Evaluate
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Evaluate d'IComparisonExpressionEvaluator pour des évaluations comparatives précises. Améliorez votre efficacité de codage grâce à notre puissant outil !
type: docs
weight: 10
url: /fr/net/aspose.words.fields/icomparisonexpressionevaluator/evaluate/
---
## IComparisonExpressionEvaluator.Evaluate method

Évalue l'expression de comparaison.

```csharp
public ComparisonEvaluationResult Evaluate(Field field, ComparisonExpression expression)
```

## Remarques

L'implémentation doit renvoyer`nul` pour indiquer que l'évaluation par défaut doit être effectuée.

## Exemples

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
    // 1. " SI {0} {1} {2} \"argument vrai\" \"argument faux\" ".
    // 2. " COMPARER {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Si le « comparisonResult » n'est pas défini, nous créons « ComparisonEvaluationResult » avec une chaîne, au lieu d'un booléen.
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

### Voir également

* class [ComparisonEvaluationResult](../../comparisonevaluationresult/)
* class [Field](../../field/)
* class [ComparisonExpression](../../comparisonexpression/)
* interface [IComparisonExpressionEvaluator](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
