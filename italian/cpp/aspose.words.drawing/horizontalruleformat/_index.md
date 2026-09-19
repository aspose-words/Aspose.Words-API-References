---
title: "Aspose::Words::Drawing::HorizontalRuleFormat class"
linktitle: "HorizontalRuleFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::HorizontalRuleFormat class. Rappresenta la formattazione della regola orizzontale. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class


Rappresenta la formattazione della regola orizzontale. Per saperne di più, visita l'articolo di documentazione [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class HorizontalRuleFormat : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Ottiene o imposta l'allineamento della regola orizzontale. |
| [get_Color](./get_color/)() | Ottiene o imposta il colore del pennello che riempie la regola orizzontale. |
| [get_Height](./get_height/)() | Ottiene o imposta l'altezza della regola orizzontale. |
| [get_NoShade](./get_noshade/)() | Indica la presenza di ombreggiatura 3D per la regola orizzontale. Se **true**, la regola orizzontale è senza ombreggiatura 3D e viene utilizzato un colore solido. |
| [get_WidthPercent](./get_widthpercent/)() | Ottiene o imposta la lunghezza della regola orizzontale specificata espressa come percentuale della larghezza della finestra. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::Drawing::HorizontalRuleAlignment) | Setter per [Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment](./get_alignment/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Drawing::HorizontalRuleFormat::get_Color](./get_color/). |
| [set_Height](./set_height/)(double) | Impostatore per [Aspose::Words::Drawing::HorizontalRuleFormat::get_Height](./get_height/). |
| [set_NoShade](./set_noshade/)(bool) | Impostatore per [Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade](./get_noshade/). |
| [set_WidthPercent](./set_widthpercent/)(double) | Impostatore per [Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent](./get_widthpercent/). |
| static [Type](./type/)() |  |

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
