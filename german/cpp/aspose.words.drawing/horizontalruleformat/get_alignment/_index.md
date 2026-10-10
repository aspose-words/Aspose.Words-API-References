---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment-Methode"
linktitle: "get_Alignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment-Methode. Ruft die Ausrichtung der horizontalen Regel in C++ ab oder legt sie fest."
type: docs
weight: 2000
url: /de/cpp/aspose.words.drawing/horizontalruleformat/get_alignment/
---
## HorizontalRuleFormat::get_Alignment method


Liest oder setzt die Ausrichtung der horizontalen Regel.

```cpp
Aspose::Words::Drawing::HorizontalRuleAlignment Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment()
```

## Hinweise


Der Standardwert ist [Left](../../horizontalrulealignment/).

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

* Enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* Class [HorizontalRuleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
