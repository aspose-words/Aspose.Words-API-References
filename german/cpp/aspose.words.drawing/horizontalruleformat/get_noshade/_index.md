---
title: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade-Methode"
linktitle: "get_NoShade"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade-Methode. Gibt an, ob eine 3D‑Schattierung für die horizontale Regel vorhanden ist. Wenn true, dann ist die horizontale Regel ohne 3D‑Schattierung und es wird eine Vollfarbe in C++ verwendet."
type: docs
weight: 5000
url: /de/cpp/aspose.words.drawing/horizontalruleformat/get_noshade/
---
## HorizontalRuleFormat::get_NoShade method


Gibt an, ob eine 3D‑Schattierung für die horizontale Regel vorhanden ist. Wenn **true**, dann hat die horizontale Regel keine 3D‑Schattierung und es wird eine Vollfarbe verwendet.

```cpp
bool Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade()
```

## Hinweise


Der Standardwert ist **false**.

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
