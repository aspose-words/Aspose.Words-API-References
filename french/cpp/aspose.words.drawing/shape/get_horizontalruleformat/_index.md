---
title: "Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat method"
linktitle: "get_HorizontalRuleFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat method. Fournit l'accès aux propriétés de la forme de règle horizontale. Pour une forme qui n'est pas une règle horizontale, renvoie null en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.drawing/shape/get_horizontalruleformat/
---
## Shape::get_HorizontalRuleFormat method


Fournit l'accès aux propriétés de la forme de règle horizontale. Pour une forme qui n'est pas une règle horizontale, renvoie **null**.

```cpp
System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat()
```


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

* Class [HorizontalRuleFormat](../../horizontalruleformat/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
