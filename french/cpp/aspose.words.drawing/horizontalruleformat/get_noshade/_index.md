---
title: "Méthode Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade"
linktitle: "get_NoShade"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade method. Indique la présence d'un ombrage 3D pour la règle horizontale. Si vrai, la règle horizontale est sans ombrage 3D et une couleur unie est utilisée en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.drawing/horizontalruleformat/get_noshade/
---
## HorizontalRuleFormat::get_NoShade method


Indique la présence d'un ombrage 3D pour la règle horizontale. Si **true**, alors la règle horizontale est sans ombrage 3D et une couleur unie est utilisée.

```cpp
bool Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade()
```

## Remarques


La valeur par défaut est **false**.

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
