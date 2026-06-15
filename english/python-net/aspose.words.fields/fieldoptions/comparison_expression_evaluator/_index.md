---
title: FieldOptions.comparison_expression_evaluator property
linktitle: comparison_expression_evaluator property
articleTitle: comparison_expression_evaluator property
second_title: Aspose.Words for Python
description: "FieldOptions.comparison_expression_evaluator property. Gets or sets the field comparison expressions evaluator."
type: docs
weight: 40
url: /python-net/aspose.words.fields/fieldoptions/comparison_expression_evaluator/
---

## FieldOptions.comparison_expression_evaluator property

Gets or sets the field comparison expressions evaluator.


```python
@property
def comparison_expression_evaluator(self) -> aspose.words.fields.IComparisonExpressionEvaluator:
    ...

@comparison_expression_evaluator.setter
def comparison_expression_evaluator(self, value: aspose.words.fields.IComparisonExpressionEvaluator):
    ...

```

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

* module [aspose.words.fields](../../)
* class [FieldOptions](../)
* class [IComparisonExpressionEvaluator](../../icomparisonexpressionevaluator/)

