---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height-Methode"
linktitle: "get_Height"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Height-Methode. Ruft die Höhe der horizontalen Regel in C++ ab oder legt sie fest."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing/horizontalruleformat/get_height/
---
## HorizontalRuleFormat::get_Height method


Liest oder setzt die Höhe der horizontalen Regel.

```cpp
double Aspose::Words::Drawing::HorizontalRuleFormat::get_Height()
```

## Hinweise


Dies ist eine Abkürzung zur [Height](../../shapebase/get_height/) Eigenschaft.

Gültige Werte liegen im Bereich von 0 bis 1584, einschließlich.

Der Standardwert ist 1,5.

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
