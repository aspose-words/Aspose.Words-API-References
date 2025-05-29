---
title: ComparisonExpression Class
linktitle: ComparisonExpression
articleTitle: ComparisonExpression
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.ComparisonExpression für effizienten Dokumentenvergleich. Verbessern Sie Ihren Workflow mit leistungsstarken Ausdrucksfunktionen!
type: docs
weight: 1900
url: /de/net/aspose.words.fields/comparisonexpression/
---
## ComparisonExpression class

Der Vergleichsausdruck.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public sealed class ComparisonExpression
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/comparisonexpression/comparisonoperator/) { get; } | Ruft den Vergleichsoperator ab. |
| [LeftExpression](../../aspose.words.fields/comparisonexpression/leftexpression/) { get; } | Ruft den linken Ausdruck ab. |
| [RightExpression](../../aspose.words.fields/comparisonexpression/rightexpression/) { get; } | Ruft den richtigen Ausdruck ab. |

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

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
