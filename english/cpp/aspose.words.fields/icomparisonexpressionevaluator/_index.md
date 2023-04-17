---
title: Aspose::Words::Fields::IComparisonExpressionEvaluator interface
linktitle: IComparisonExpressionEvaluator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::IComparisonExpressionEvaluator interface. When implemented, allows to override default comparison expressions evaluation for the FieldIf and FieldCompare fields in C++.'
type: docs
weight: 119000
url: /cpp/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface


When implemented, allows to override default comparison expressions evaluation for the [FieldIf](../fieldif/) and [FieldCompare](../fieldcompare/) fields.

```cpp
class IComparisonExpressionEvaluator : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [Evaluate](./evaluate/)(System::SharedPtr\<Aspose::Words::Fields::Field\>, System::SharedPtr\<Aspose::Words::Fields::ComparisonExpression\>) | Evaluates comparison expression. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
