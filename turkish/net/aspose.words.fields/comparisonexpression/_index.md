---
title: ComparisonExpression Class
linktitle: ComparisonExpression
articleTitle: ComparisonExpression
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.ComparisonExpression sınıf. Karşılaştırma ifadesi C#'da.
type: docs
weight: 1490
url: /tr/net/aspose.words.fields/comparisonexpression/
---
## ComparisonExpression class

Karşılaştırma ifadesi.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public sealed class ComparisonExpression
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/comparisonexpression/comparisonoperator/) { get; } | Karşılaştırma operatörünü alır. |
| [LeftExpression](../../aspose.words.fields/comparisonexpression/leftexpression/) { get; } | Soldaki ifadeyi alır. |
| [RightExpression](../../aspose.words.fields/comparisonexpression/rightexpression/) { get; } | Doğru ifadeyi alır. |

## Örnekler

IF ve COMPARE alanları için özel değerlendirmenin nasıl uygulanacağını gösterir.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // Bu örnekte kullandığımız alan kodları:
    // 1. " IF {0} {1} {2} \"doğru argüman\" \"yanlış argüman\" ".
    // 2. " KARŞILAŞTIRIN {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // "ComparisonEvaluationResult" tanımsızsa bool yerine string ile "ComparisonEvaluationResult" oluştururuz.
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
/// FieldIf ve FieldCompare için karşılaştırma ifadelerinin değerlendirilmesi.
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

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
