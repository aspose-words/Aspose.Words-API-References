---
title: "Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat Methode"
linktitle: "get_HorizontalRuleFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat-Methode. Stellt Zugriff auf die Eigenschaften der horizontalen Regel‑Form bereit. Für eine Form, die keine horizontale Regel ist, wird null in C++ zurückgegeben."
type: docs
weight: 12000
url: /de/cpp/aspose.words.drawing/shape/get_horizontalruleformat/
---
## Shape::get_HorizontalRuleFormat method


Bietet Zugriff auf die Eigenschaften der horizontalen Linienform. Für eine Form, die keine horizontale Linie ist, wird **null** zurückgegeben.

```cpp
System::SharedPtr<Aspose::Words::Drawing::HorizontalRuleFormat> Aspose::Words::Drawing::Shape::get_HorizontalRuleFormat()
```


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

* Class [HorizontalRuleFormat](../../horizontalruleformat/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
