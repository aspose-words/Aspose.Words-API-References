---
title: "Aspose::Words::Drawing::HorizontalRuleFormat class"
linktitle: "HorizontalRuleFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat class. Représente le formatage de la règle horizontale. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class


Représente le format de la règle horizontale. Pour en savoir plus, consultez l'article de documentation [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class HorizontalRuleFormat : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Obtient ou définit l'alignement de la règle horizontale. |
| [get_Color](./get_color/)() | Obtient ou définit la couleur du pinceau qui remplit la règle horizontale. |
| [get_Height](./get_height/)() | Obtient ou définit la hauteur de la règle horizontale. |
| [get_NoShade](./get_noshade/)() | Indique la présence d'un ombrage 3D pour la règle horizontale. Si **true**, alors la règle horizontale est sans ombrage 3D et une couleur unie est utilisée. |
| [get_WidthPercent](./get_widthpercent/)() | Obtient ou définit la longueur de la règle horizontale spécifiée exprimée en pourcentage de la largeur de la fenêtre. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::Drawing::HorizontalRuleAlignment) | Définisseur pour [Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment](./get_alignment/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Drawing::HorizontalRuleFormat::get_Color](./get_color/). |
| [set_Height](./set_height/)(double) | Définisseur pour [Aspose::Words::Drawing::HorizontalRuleFormat::get_Height](./get_height/). |
| [set_NoShade](./set_noshade/)(bool) | Définisseur pour [Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade](./get_noshade/). |
| [set_WidthPercent](./set_widthpercent/)(double) | Définisseur pour [Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent](./get_widthpercent/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
