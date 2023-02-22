---
title: Class ComparisonEvaluationResult
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.ComparisonEvaluationResult сорт. Результат оценки сравнения.
type: docs
weight: 1330
url: /ru/net/aspose.words.fields/comparisonevaluationresult/
---
## ComparisonEvaluationResult class

Результат оценки сравнения.

```csharp
public sealed class ComparisonEvaluationResult
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [ComparisonEvaluationResult](comparisonevaluationresult/#constructor)(bool) | Создает результат оценки сравнения. |
| [ComparisonEvaluationResult](comparisonevaluationresult/#constructor_1)(string) | Создает ошибочный результат оценки сравнения с соответствующим сообщением об ошибке. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ErrorMessage](../../aspose.words.fields/comparisonevaluationresult/errormessage/) { get; } | Получает сообщение об ошибке неудачного результата оценки сравнения. |
| [Result](../../aspose.words.fields/comparisonevaluationresult/result/) { get; } | Получает результат оценки сравнения. |

### Примеры

Показывает, как реализовать пользовательскую оценку для полей ЕСЛИ и СРАВНИТЬ.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // Коды полей, которые мы используем в этом примере:
    // 1. " ЕСЛИ {0} {1} {2} \"верный аргумент\" \"ложный аргумент\" ".
    // 2. "СРАВНИТЬ {0} {1} {2}".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // Если "comparisonResult" не определен, мы создаем "ComparisonEvaluationResult" со строкой вместо логического значения.
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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


