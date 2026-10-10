---
title: "Aspose::Words::Drawing::Shape::get_Adjustments method"
linktitle: "get_Adjustments"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Shape::get_Adjustments method. Fournit l'accès aux valeurs brutes d'ajustement d'une forme. Pour une forme qui ne contient aucune valeur brute d'ajustement, elle renvoie une collection vide en C++."
type: docs
weight: 3834
url: /fr/cpp/aspose.words.drawing/shape/get_adjustments/
---
## Shape::get_Adjustments method


Fournit l'accès aux valeurs brutes d'ajustement d'une forme. Pour une forme qui ne contient aucune valeur brute d'ajustement, elle renvoie une collection vide.

```cpp
System::SharedPtr<Aspose::Words::Drawing::AdjustmentCollection> Aspose::Words::Drawing::Shape::get_Adjustments()
```


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

* Class [AdjustmentCollection](../../adjustmentcollection/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
