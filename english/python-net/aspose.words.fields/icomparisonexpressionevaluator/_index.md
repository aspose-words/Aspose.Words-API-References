---
title: IComparisonExpressionEvaluator class
linktitle: IComparisonExpressionEvaluator class
articleTitle: IComparisonExpressionEvaluator class
second_title: Aspose.Words for Python
description: "aspose.words.fields.IComparisonExpressionEvaluator class. When implemented, allows to override default comparison expressions evaluation for the [FieldIf](../fieldif/) and [FieldCompare](../fieldcompare/) fields."
type: docs
weight: 1220
url: /python-net/aspose.words.fields/icomparisonexpressionevaluator/
---

## IComparisonExpressionEvaluator class

When implemented, allows to override default comparison expressions evaluation for the [FieldIf](../fieldif/) and [FieldCompare](../fieldcompare/) fields.



### Methods

| Name | Description |
| --- | --- |
|[ evaluate(field, expression)](./evaluate/#field_comparisonexpression) | Evaluates comparison expression. |

### Examples

Shows how to implement custom evaluation for the IF and COMPARE fields (ComparisonExpressionEvaluator).

```python
class ComparisonExpressionEvaluator(aw.fields.IComparisonExpressionEvaluator):

    def __init__(self, result):
        self.m_invocations = []
        self.m_result = result
        if self.m_result != None:
            print(self.m_result.error_message)
            print(self.m_result.result)

    def evaluate(self, field, expression):
        self.m_invocations.append([expression.left_expression, expression.comparison_operator, expression.right_expression])
        return self.m_result

    def assert_invocations_count(self, expected):
        self.assertEqual(expected, len(self.m_invocations))
        return self

    def assert_invocation_arguments(self, invocation_index, expected_left_expression, expected_comparison_operator, expected_right_expression):
        arguments = self.m_invocations[invocation_index]
        self.assertEqual(expected_left_expression, arguments[0])
        self.assertEqual(expected_comparison_operator, arguments[1])
        self.assertEqual(expected_right_expression, arguments[2])
        return self
```

### See Also

* module [aspose.words.fields](../)
* property [FieldOptions.comparison_expression_evaluator](../fieldoptions/comparison_expression_evaluator/)

