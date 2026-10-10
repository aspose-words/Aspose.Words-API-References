---
title: "Aspose::Words::Fields::IComparisonExpressionEvaluator-gränssnitt"
linktitle: "IComparisonExpressionEvaluator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::IComparisonExpressionEvaluator-gränssnitt. När det implementeras möjliggör det att åsidosätta standardutvärderingen av jämförelseuttryck för FieldIf- och FieldCompare-fälten i C++."
type: docs
weight: 119000
url: /sv/cpp/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface


När den implementeras möjliggör den att åsidosätta standardutvärderingen av jämförelseuttryck för fälten [FieldIf](../fieldif/) och [FieldCompare](../fieldcompare/).

```cpp
class IComparisonExpressionEvaluator : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [Evaluate](./evaluate/)(System::SharedPtr\<Aspose::Words::Fields::Field\>, System::SharedPtr\<Aspose::Words::Fields::ComparisonExpression\>) | Utvärderar jämförelseuttrycket. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
