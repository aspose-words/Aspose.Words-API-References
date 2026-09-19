---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment metodo"
linktitle: "get_Alignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment metodo. Ottiene o imposta l'allineamento della linea orizzontale in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing/horizontalruleformat/get_alignment/
---
## HorizontalRuleFormat::get_Alignment method


Ottiene o imposta l'allineamento della regola orizzontale.

```cpp
Aspose::Words::Drawing::HorizontalRuleAlignment Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment()
```

## Note


Il valore predefinito è [Left](../../horizontalrulealignment/).

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

* Enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
