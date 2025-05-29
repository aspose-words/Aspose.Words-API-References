---
title: IComparisonExpressionEvaluator Interface
linktitle: IComparisonExpressionEvaluator
articleTitle: IComparisonExpressionEvaluator
second_title: Aspose.Words для .NET
description: Улучшите обработку документов с помощью Aspose.Words.Fields.IComparisonExpressionEvaluator. Настройте сравнительные оценки для полей FieldIf и FieldCompare без особых усилий!
type: docs
weight: 3090
url: /ru/net/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface

При реализации позволяет переопределить оценку выражений сравнения по умолчанию для[`FieldIf`](../fieldif/) и[`FieldCompare`](../fieldcompare/) поля.

```csharp
public interface IComparisonExpressionEvaluator
```

## Методы

| Имя | Описание |
| --- | --- |
| [Evaluate](../../aspose.words.fields/icomparisonexpressionevaluator/evaluate/)(*[Field](../field/), [ComparisonExpression](../comparisonexpression/)*) | Оценивает выражение сравнения. |

## Примеры

Показывает, как реализовать пользовательскую оценку для полей IF и COMPARE.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // Коды полей, которые мы используем в этом примере:
    // 1. "ЕСЛИ {0} {1} {2} \"истинный аргумент\" \"ложный аргумент\" ".
    // 2. "СРАВНИТЬ {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Если "comparisonResult" не определен, мы создаем "ComparisonEvaluationResult" со строкой, а не с логическим значением.
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
/// Оценка выражений сравнения для FieldIf и FieldCompare.
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

### Смотрите также

* property [ComparisonExpressionEvaluator](../fieldoptions/comparisonexpressionevaluator/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
