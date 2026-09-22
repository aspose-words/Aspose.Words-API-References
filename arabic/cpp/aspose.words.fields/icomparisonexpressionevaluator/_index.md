---
title: "واجهة Aspose::Words::Fields::IComparisonExpressionEvaluator"
linktitle: "IComparisonExpressionEvaluator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::Fields::IComparisonExpressionEvaluator. عند تنفيذها، تسمح بتجاوز تقييم تعبيرات المقارنة الافتراضية لحقلي FieldIf و FieldCompare في C++."
type: docs
weight: 119000
url: /ar/cpp/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface


عند تنفيذها، تسمح بتجاوز تقييم تعبيرات المقارنة الافتراضية لحقلي [FieldIf](../fieldif/) و [FieldCompare](../fieldcompare/).

```cpp
class IComparisonExpressionEvaluator : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [Evaluate](./evaluate/)(System::SharedPtr\<Aspose::Words::Fields::Field\>, System::SharedPtr\<Aspose::Words::Fields::ComparisonExpression\>) | يقيم تعبير المقارنة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
