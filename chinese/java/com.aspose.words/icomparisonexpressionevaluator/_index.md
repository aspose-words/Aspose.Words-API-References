---
title: IComparisonExpressionEvaluator
second_title: Aspose.Words for Java API 参考
description: 实现时允许覆盖和字段的默认比较表达式评估。
type: docs
weight: 634
url: /zh/java/com.aspose.words/icomparisonexpressionevaluator/
---
```
public interface IComparisonExpressionEvaluator
```

实施时，允许覆盖默认比较表达式评估[FieldIf](../../com.aspose.words/fieldif)和[FieldCompare](../../com.aspose.words/fieldcompare)字段。
## 方法

| 方法 | 描述 |
| --- | --- |
| [evaluate(Field field, ComparisonExpression expression)](#evaluate-com.aspose.words.Field-com.aspose.words.ComparisonExpression-) | 评估比较表达式。 |
### evaluate(Field field, ComparisonExpression expression) {#evaluate-com.aspose.words.Field-com.aspose.words.ComparisonExpression-}
```
public abstract ComparisonEvaluationResult evaluate(Field field, ComparisonExpression expression)
```


评估比较表达式。实现应该返回**null**表示应执行默认评估。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) |  |
| expression | [ComparisonExpression](../../com.aspose.words/comparisonexpression) |  |

**退货:**
[ComparisonEvaluationResult](../../com.aspose.words/comparisonevaluationresult)