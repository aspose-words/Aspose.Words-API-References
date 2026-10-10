---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent méthode"
linktitle: "get_WidthPercent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent méthode. Obtient ou définit la longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.drawing/horizontalruleformat/get_widthpercent/
---
## HorizontalRuleFormat::get_WidthPercent method


Obtient ou définit la longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent()
```

## Remarques


Les valeurs valides vont de 1 à 100 inclus.

La valeur par défaut est 100.

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
