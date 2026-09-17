---
title: "Aspose::Words::DocumentBuilder::InsertHorizontalRule méthode"
linktitle: "InsertHorizontalRule"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertHorizontalRule méthode. Insère une forme de règle horizontale dans le document en C++."
type: docs
weight: 36000
url: /fr/cpp/aspose.words/documentbuilder/inserthorizontalrule/
---
## DocumentBuilder::InsertHorizontalRule method


Insère une forme de règle horizontale dans le document.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertHorizontalRule()
```


### ReturnValue

La forme qui est une règle horizontale.

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

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
