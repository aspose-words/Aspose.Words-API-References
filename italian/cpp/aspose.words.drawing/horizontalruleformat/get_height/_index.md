---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height metodo"
linktitle: "get_Height"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height metodo. Ottiene o imposta l'altezza della linea orizzontale in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.drawing/horizontalruleformat/get_height/
---
## HorizontalRuleFormat::get_Height method


Ottiene o imposta l'altezza della regola orizzontale.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_Height()
```

## Note


Questo è un collegamento rapido alla proprietà [Height](../../shapebase/get_height/).

I valori validi vanno da 0 a 1584 inclusi.

Il valore predefinito è 1.5.

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
