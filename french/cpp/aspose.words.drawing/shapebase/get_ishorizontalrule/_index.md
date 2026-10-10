---
title: "Méthode Aspose::Words::Drawing::ShapeBase::get_IsHorizontalRule"
linktitle: "get_IsHorizontalRule"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsHorizontalRule méthode. Retourne true si cette forme est une règle horizontale en C++."
type: docs
weight: 28000
url: /fr/cpp/aspose.words.drawing/shapebase/get_ishorizontalrule/
---
## ShapeBase::get_IsHorizontalRule method


Renvoie **true** si cette forme est une règle horizontale.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsHorizontalRule()
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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
