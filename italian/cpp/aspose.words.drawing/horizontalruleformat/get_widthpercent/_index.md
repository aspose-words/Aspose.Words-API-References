---
title: "Metodo Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent"
linktitle: "get_WidthPercent"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent. Ottiene o imposta la lunghezza della linea orizzontale specificata espressa come percentuale della larghezza della finestra in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.drawing/horizontalruleformat/get_widthpercent/
---
## HorizontalRuleFormat::get_WidthPercent method


Ottiene o imposta la lunghezza della regola orizzontale specificata espressa come percentuale della larghezza della finestra.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent()
```

## Note


I valori validi vanno da 1 a 100 inclusi.

Il valore predefinito è 100.

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
