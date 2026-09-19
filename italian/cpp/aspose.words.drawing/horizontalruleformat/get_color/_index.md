---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Color metodo"
linktitle: "get_Color"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Color metodo. Ottiene o imposta il colore del pennello che riempie la linea orizzontale in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing/horizontalruleformat/get_color/
---
## HorizontalRuleFormat::get_Color method


Ottiene o imposta il colore del pennello che riempie la regola orizzontale.

```cpp
System::Drawing::Color Aspose::Words::Drawing::HorizontalRuleFormat::get_Color()
```

## Note


Questo è un collegamento rapido alla proprietà [Color](../../fill/get_color/).

Il valore predefinito è **Gray**.

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
