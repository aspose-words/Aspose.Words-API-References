---
title: "Aspose::Words::Drawing::HorizontalRuleAlignment enum"
linktitle: "HorizontalRuleAlignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::HorizontalRuleAlignment enum. Représente l'alignement de la règle horizontale spécifiée en C++."
type: docs
weight: 27000
url: /fr/cpp/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enum


Représente l'alignement pour la règle horizontale spécifiée.

```cpp
enum class HorizontalRuleAlignment
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Gauche | 0 | Aligné à gauche. |
| Centre | 1 | Aligné au centre. |
| Droite | 2 | Aligné à droite. |


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
