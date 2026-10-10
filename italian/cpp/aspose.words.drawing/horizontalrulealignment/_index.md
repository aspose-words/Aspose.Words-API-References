---
title: "Aspose::Words::Drawing::HorizontalRuleAlignment enum"
linktitle: "HorizontalRuleAlignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::HorizontalRuleAlignment enum. Rappresenta l'allineamento per la regola orizzontale specificata in C++."
type: docs
weight: 27000
url: /it/cpp/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enum


Rappresenta l'allineamento per la regola orizzontale specificata.

```cpp
enum class HorizontalRuleAlignment
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Sinistra | 0 | Allineato a sinistra. |
| Centro | 1 | Allineato al centro. |
| Destra | 2 | Allineato a destra. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
