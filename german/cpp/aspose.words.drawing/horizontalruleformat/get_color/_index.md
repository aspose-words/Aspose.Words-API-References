---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Color Methode"
linktitle: "get_Color"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_Color-Methode. Ruft die Pinsel­farbe ab oder legt sie fest, die die horizontale Regel in C++ füllt."
type: docs
weight: 3000
url: /de/cpp/aspose.words.drawing/horizontalruleformat/get_color/
---
## HorizontalRuleFormat::get_Color method


Liest oder setzt die Pinsel‑Farbe, die die horizontale Regel füllt.

```cpp
System::Drawing::Color Aspose::Words::Drawing::HorizontalRuleFormat::get_Color()
```

## Hinweise


Dies ist eine Abkürzung zur [Color](../../fill/get_color/) Eigenschaft.

Der Standardwert ist **Gray**.

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
