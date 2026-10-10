---
title: "Interfaccia Aspose::Words::Fields::IComparisonExpressionEvaluator"
linktitle: "IComparisonExpressionEvaluator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::Fields::IComparisonExpressionEvaluator. Quando implementata, consente di sovrascrivere la valutazione predefinita delle espressioni di confronto per i campi FieldIf e FieldCompare in C++."
type: docs
weight: 119000
url: /it/cpp/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface


Quando implementata, consente di sovrascrivere la valutazione predefinita delle espressioni di confronto per i campi [FieldIf](../fieldif/) e [FieldCompare](../fieldcompare/).

```cpp
class IComparisonExpressionEvaluator : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [Evaluate](./evaluate/)(System::SharedPtr\<Aspose::Words::Fields::Field\>, System::SharedPtr\<Aspose::Words::Fields::ComparisonExpression\>) | Valuta l'espressione di confronto. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
