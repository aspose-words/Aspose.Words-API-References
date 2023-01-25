---
title: IComparisonExpressionEvaluator
second_title: Aspose.Words for Java API Reference
description: When implemented allows to override default comparison expressions evaluation for the  and  fields.
type: docs
weight: 638
url: /java/com.aspose.words/icomparisonexpressionevaluator/
---
```
public interface IComparisonExpressionEvaluator
```

When implemented, allows to override default comparison expressions evaluation for the [FieldIf](../../com.aspose.words/fieldif) and [FieldCompare](../../com.aspose.words/fieldcompare) fields.
## Methods

| Method | Description |
| --- | --- |
| [evaluate(Field field, ComparisonExpression expression)](#evaluate-com.aspose.words.Field-com.aspose.words.ComparisonExpression) | Evaluates comparison expression. |
### evaluate(Field field, ComparisonExpression expression) {#evaluate-com.aspose.words.Field-com.aspose.words.ComparisonExpression}
```
public abstract ComparisonEvaluationResult evaluate(Field field, ComparisonExpression expression)
```


Evaluates comparison expression. The implementation should return  null  to indicate that the default evaluation should be performed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) |  |
| expression | [ComparisonExpression](../../com.aspose.words/comparisonexpression) |  |

**Returns:**
[ComparisonEvaluationResult](../../com.aspose.words/comparisonevaluationresult)
