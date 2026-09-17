---
title: "Méthode Aspose::Words::Drawing::AdjustmentCollection::idx_get"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::AdjustmentCollection::idx_get. Retourne un ajustement à l'index spécifié en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.drawing/adjustmentcollection/idx_get/
---
## AdjustmentCollection::idx_get method


Renvoie un ajustement à l'index spécifié.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Adjustment> Aspose::Words::Drawing::AdjustmentCollection::idx_get(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Un index dans la collection. |

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

* Class [Adjustment](../../adjustment/)
* Class [AdjustmentCollection](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
