---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade metodo"
linktitle: "get_NoShade"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade. Indica la presenza di ombreggiatura 3D per la linea orizzontale. Se vero, la linea orizzontale è senza ombreggiatura 3D e viene usato un colore solido in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.drawing/horizontalruleformat/get_noshade/
---
## HorizontalRuleFormat::get_NoShade method


Indica la presenza di ombreggiatura 3D per la regola orizzontale. Se **true**, la regola orizzontale è senza ombreggiatura 3D e viene utilizzato un colore solido.

```cpp
bool Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade()
```

## Note


Il valore predefinito è **false**.

## Esempi



Mostra come inserire una forma di regola orizzontale e personalizzare la sua formattazione.
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

## Vedi anche

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
