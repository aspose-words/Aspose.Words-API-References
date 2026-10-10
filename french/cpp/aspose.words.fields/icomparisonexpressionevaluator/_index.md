---
title: "Interface Aspose::Words::Fields::IComparisonExpressionEvaluator"
linktitle: "IComparisonExpressionEvaluator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Interface Aspose::Words::Fields::IComparisonExpressionEvaluator. Lorsqu'elle est implémentée, elle permet de remplacer l'évaluation par défaut des expressions de comparaison pour les champs FieldIf et FieldCompare en C++."
type: docs
weight: 119000
url: /fr/cpp/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface


Lorsqu'elle est implémentée, elle permet de remplacer l'évaluation par défaut des expressions de comparaison pour les champs [FieldIf](../fieldif/) et [FieldCompare](../fieldcompare/).

```cpp
class IComparisonExpressionEvaluator : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [Evaluate](./evaluate/)(System::SharedPtr\<Aspose::Words::Fields::Field\>, System::SharedPtr\<Aspose::Words::Fields::ComparisonExpression\>) | Évalue l'expression de comparaison. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
