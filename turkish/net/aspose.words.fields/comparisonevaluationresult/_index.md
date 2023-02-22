---
title: Class ComparisonEvaluationResult
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.ComparisonEvaluationResult sınıf. Karşılaştırma değerlendirme sonucu.
type: docs
weight: 1330
url: /tr/net/aspose.words.fields/comparisonevaluationresult/
---
## ComparisonEvaluationResult class

Karşılaştırma değerlendirme sonucu.

```csharp
public sealed class ComparisonEvaluationResult
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ComparisonEvaluationResult](comparisonevaluationresult/#constructor)(bool) | Bir karşılaştırma değerlendirme sonucu oluşturur. |
| [ComparisonEvaluationResult](comparisonevaluationresult/#constructor_1)(string) | Karşılık gelen hata mesajıyla başarısız bir karşılaştırma değerlendirme sonucu oluşturur. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ErrorMessage](../../aspose.words.fields/comparisonevaluationresult/errormessage/) { get; } | Başarısız karşılaştırma değerlendirme sonucunun hata mesajını alır. |
| [Result](../../aspose.words.fields/comparisonevaluationresult/result/) { get; } | Karşılaştırma değerlendirme sonucunu alır. |

### Örnekler

EĞER ve KARŞILAŞTIR alanları için özel değerlendirmenin nasıl uygulanacağını gösterir.

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
    // 2. " KARŞILAŞTIR {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // "comparisonResult" tanımsız ise bool yerine string ile "ComparisonEvaluationResult" yaratırız.
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
/// FieldIf ve FieldCompare için karşılaştırma ifadeleri değerlendirmesi.
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


