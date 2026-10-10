---
title: "Aspose::Words::Fields::IComparisonExpressionEvaluator interfaz"
linktitle: "IComparisonExpressionEvaluator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::IComparisonExpressionEvaluator interfaz. Cuando se implementa, permite sobrescribir la evaluación predeterminada de expresiones de comparación para los campos FieldIf y FieldCompare en C++."
type: docs
weight: 119000
url: /es/cpp/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface


Cuando se implementa, permite sobrescribir la evaluación predeterminada de expresiones de comparación para los campos [FieldIf](../fieldif/) y [FieldCompare](../fieldcompare/).

```cpp
class IComparisonExpressionEvaluator : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [Evaluate](./evaluate/)(System::SharedPtr\<Aspose::Words::Fields::Field\>, System::SharedPtr\<Aspose::Words::Fields::ComparisonExpression\>) | Evalúa la expresión de comparación. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
