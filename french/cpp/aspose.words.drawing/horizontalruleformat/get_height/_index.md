---
title: "Méthode Aspose::Words::Drawing::HorizontalRuleFormat::get_Height"
linktitle: "get_Height"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::HorizontalRuleFormat::get_Height. Obtient ou définit la hauteur de la règle horizontale en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.drawing/horizontalruleformat/get_height/
---
## HorizontalRuleFormat::get_Height method


Obtient ou définit la hauteur de la règle horizontale.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_Height()
```

## Remarques


Ceci est un raccourci vers la propriété [Height](../../shapebase/get_height/).

Les valeurs valides vont de 0 à 1584 inclus.

La valeur par défaut est 1,5.

## Exemples



Montre comment insérer une forme de règle horizontale et personnaliser son formatage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertHorizontalRule();

System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> horizontalRuleFormat = shape->get_HorizontalRuleFormat();
horizontalRuleFormat->set_Alignment(Aspose::Words::Drawing::HorizontalRuleAlignment::Center);
horizontalRuleFormat->set_WidthPercent(70);
horizontalRuleFormat->set_Height(3);
horizontalRuleFormat->set_Color(System::Drawing::Color::get_Blue());
horizontalRuleFormat->set_NoShade(true);

ASSERT_TRUE(shape->get_IsHorizontalRule());
ASSERT_TRUE(shape->get_HorizontalRuleFormat()->get_NoShade());
```

## Voir aussi

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
