---
title: "Aspose::Words::Drawing::HorizontalRuleAlignment enum"
linktitle: "HorizontalRuleAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::HorizontalRuleAlignment enum. Stellt die Ausrichtung für die angegebene horizontale Regel in C++ dar."
type: docs
weight: 27000
url: /de/cpp/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enum


Stellt die Ausrichtung für die angegebene horizontale Regel dar.

```cpp
enum class HorizontalRuleAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Links | 0 | Links ausgerichtet. |
| Mitte | 1 | Zentriert ausgerichtet. |
| Rechts | 2 | Rechts ausgerichtet. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
