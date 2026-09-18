---
title: "Aspose::Words::Fields::IComparisonExpressionEvaluator Schnittstelle"
linktitle: "IComparisonExpressionEvaluator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::IComparisonExpressionEvaluator Schnittstelle. Wenn implementiert, ermöglicht sie das Überschreiben der Standardauswertung von Vergleichsausdrücken für die FieldIf- und FieldCompare-Felder in C++."
type: docs
weight: 119000
url: /de/cpp/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface


Wenn implementiert, ermöglicht es das Überschreiben der Standardauswertung von Vergleichsausdrücken für die [FieldIf](../fieldif/)- und [FieldCompare](../fieldcompare/)-Felder.

```cpp
class IComparisonExpressionEvaluator : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [Evaluate](./evaluate/)(System::SharedPtr\<Aspose::Words::Fields::Field\>, System::SharedPtr\<Aspose::Words::Fields::ComparisonExpression\>) | Wertet den Vergleichsausdruck aus. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
