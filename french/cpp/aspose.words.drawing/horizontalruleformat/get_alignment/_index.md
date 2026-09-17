---
title: "Méthode Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment"
linktitle: "get_Alignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment. Obtient ou définit l'alignement de la règle horizontale en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing/horizontalruleformat/get_alignment/
---
## HorizontalRuleFormat::get_Alignment method


Obtient ou définit l'alignement de la règle horizontale.

```cpp
Aspose::Words::Drawing::HorizontalRuleAlignment Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment()
```

## Remarques


La valeur par défaut est [Left](../../horizontalrulealignment/).

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

* Enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
