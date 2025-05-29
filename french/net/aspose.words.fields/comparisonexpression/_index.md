---
title: ComparisonExpression Class
linktitle: ComparisonExpression
articleTitle: ComparisonExpression
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.ComparisonExpression pour une comparaison efficace des documents. Améliorez votre flux de travail grâce à de puissantes fonctionnalités d'expression !
type: docs
weight: 1900
url: /fr/net/aspose.words.fields/comparisonexpression/
---
## ComparisonExpression class

L'expression de comparaison.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public sealed class ComparisonExpression
```

## Propriétés

| Nom | La description |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/comparisonexpression/comparisonoperator/) { get; } | Obtient l'opérateur de comparaison. |
| [LeftExpression](../../aspose.words.fields/comparisonexpression/leftexpression/) { get; } | Obtient l'expression de gauche. |
| [RightExpression](../../aspose.words.fields/comparisonexpression/rightexpression/) { get; } | Obtient la bonne expression. |

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

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
