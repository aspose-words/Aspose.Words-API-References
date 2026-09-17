---
title: "Aspose::Words::Drawing::AdjustmentCollection classe"
linktitle: "AdjustmentCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::AdjustmentCollection classe. Représente une collection en lecture seule de valeurs d'ajustement Adjustment qui sont appliquées à la forme spécifiée en C++."
type: docs
weight: 667
url: /fr/cpp/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class


Représente une collection en lecture seule de valeurs d'ajustement [Adjustment](../adjustment/) qui sont appliquées à la forme spécifiée.

```cpp
class AdjustmentCollection : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Count](./get_count/)() | Obtient le nombre d’éléments contenus dans la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Renvoie un ajustement à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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
