---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent-Methode"
linktitle: "get_WidthPercent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent Methode. Ruft die Länge der angegebenen horizontalen Regel ab oder legt sie fest, ausgedrückt als Prozentsatz der Fensterbreite in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing/horizontalruleformat/get_widthpercent/
---
## HorizontalRuleFormat::get_WidthPercent method


Liest oder setzt die Länge der angegebenen horizontalen Regel, ausgedrückt als Prozentsatz der Fensterbreite.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent()
```

## Hinweise


Gültige Werte liegen inklusiv zwischen 1 und 100.

Der Standardwert ist 100.

## Beispiele



Zeigt, wie man eine horizontale Regel‑Form einfügt und deren Formatierung anpasst.
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

## Siehe auch

* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
