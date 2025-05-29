---
title: ComparisonEvaluationResult.Result
linktitle: Result
articleTitle: Result
second_title: .NET için Aspose.Words
description: Değerlendirme sonuçlarına kolayca erişmek ve analiz etmek, veri içgörülerinizi ve karar alma yeteneğinizi geliştirmek için ComparisonEvaluationResult özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/comparisonevaluationresult/result/
---
## ComparisonEvaluationResult.Result property

Karşılaştırma değerlendirme sonucunu alır.

```csharp
public bool Result { get; }
```

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
    // 1. " EĞER {0} {1} {2} \"doğru argüman\" \"yanlış argüman\" ".
    // 2. " {0} {1} {2}'yi KARŞILAŞTIR ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Eğer "comparisonResult" tanımsızsa, "ComparisonEvaluationResult"u bool yerine string ile oluşturuyoruz.
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

### Ayrıca bakınız

* class [ComparisonEvaluationResult](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
