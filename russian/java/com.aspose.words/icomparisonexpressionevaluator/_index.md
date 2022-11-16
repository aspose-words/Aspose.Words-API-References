---
title: IComparisonExpressionEvaluator
second_title: Справочник по API Aspose.Words для Java
description: При реализации позволяет переопределить оценку выражений сравнения по умолчанию для полей и .
type: docs
weight: 634
url: /ru/java/com.aspose.words/icomparisonexpressionevaluator/
---
```
public interface IComparisonExpressionEvaluator
```

 При реализации позволяет переопределить оценку выражений сравнения по умолчанию для[FieldIf](../../com.aspose.words/fieldif) а также[FieldCompare](../../com.aspose.words/fieldcompare) поля.
## Методы

| Метод | Описание |
| --- | --- |
| [evaluate(Field field, ComparisonExpression expression)](#evaluate-com.aspose.words.Field-com.aspose.words.ComparisonExpression-) | Вычисляет выражение сравнения. |
### evaluate(Field field, ComparisonExpression expression) {#evaluate-com.aspose.words.Field-com.aspose.words.ComparisonExpression-}
```
public abstract ComparisonEvaluationResult evaluate(Field field, ComparisonExpression expression)
```


 Вычисляет выражение сравнения. Реализация должна вернуться**null** чтобы указать, что должна быть выполнена оценка по умолчанию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) |  |
| expression | [ComparisonExpression](../../com.aspose.words/comparisonexpression) |  |

**Возвращает:**
[ComparisonEvaluationResult](../../com.aspose.words/comparisonevaluationresult)