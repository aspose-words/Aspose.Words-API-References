---
title: "Aspose::Words::Drawing::Adjustment class"
linktitle: "Adjustment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Adjustment class. Représente les valeurs d'ajustement qui sont appliquées à la forme spécifiée en C++."
type: docs
weight: 334
url: /fr/cpp/aspose.words.drawing/adjustment/
---
## Adjustment class


Représente les valeurs d'ajustement appliquées à la forme spécifiée.

```cpp
class Adjustment : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Name](./get_name/)() const | Obtient le nom de l'ajustement. |
| [get_Value](./get_value/)() const | Obtient ou définit la valeur brute de l'ajustement. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Adjustment::get_Value](./get_value/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment travailler avec les valeurs brutes d'ajustement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rounded rectangle shape.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> adjustments = shape->get_Adjustments();
ASSERT_EQ(1, adjustments->get_Count());

System::SharedPtr<Aspose::Words::Drawing::Adjustment> adjustment = adjustments->idx_get(0);
ASSERT_EQ(u"adj", adjustment->get_Name());
ASSERT_EQ(16667, adjustment->get_Value());

adjustment->set_Value(30000);

doc->Save(get_ArtifactsDir() + u"Shape.Adjustments.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
