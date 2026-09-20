---
title: "Интерфейс Aspose::Words::Fields::IComparisonExpressionEvaluator"
linktitle: "IComparisonExpressionEvaluator"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::Fields::IComparisonExpressionEvaluator. При реализации позволяет переопределить оценку выражений сравнения по умолчанию для полей FieldIf и FieldCompare в C++."
type: docs
weight: 119000
url: /ru/cpp/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface


При реализации позволяет переопределить оценку выражений сравнения по умолчанию для полей [FieldIf](../fieldif/) и [FieldCompare](../fieldcompare/).

```cpp
class IComparisonExpressionEvaluator : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [Evaluate](./evaluate/)(System::SharedPtr\<Aspose::Words::Fields::Field\>, System::SharedPtr\<Aspose::Words::Fields::ComparisonExpression\>) | Оценивает выражение сравнения. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
