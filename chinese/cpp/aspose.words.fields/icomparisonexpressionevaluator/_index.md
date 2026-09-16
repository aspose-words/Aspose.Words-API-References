---
title: "Aspose::Words::Fields::IComparisonExpressionEvaluator interface"
linktitle: "IComparisonExpressionEvaluator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IComparisonExpressionEvaluator 接口。实现后，可在 C++ 中覆盖 FieldIf 和 FieldCompare 字段的默认比较表达式评估。"
type: docs
weight: 119000
url: /zh/cpp/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface


实现后，可覆盖 [FieldIf](../fieldif/) 和 [FieldCompare](../fieldcompare/) 字段的默认比较表达式评估。

```cpp
class IComparisonExpressionEvaluator : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [Evaluate](./evaluate/)(System::SharedPtr\<Aspose::Words::Fields::Field\>, System::SharedPtr\<Aspose::Words::Fields::ComparisonExpression\>) | 评估比较表达式。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
