---
title: "Aspose::Words::Drawing::HorizontalRuleFormat Klasse"
linktitle: "HorizontalRuleFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::HorizontalRuleFormat Klasse. Stellt die Formatierung der horizontalen Regel dar. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class


Stellt die Formatierung einer horizontalen Linie dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class HorizontalRuleFormat : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Liest oder setzt die Ausrichtung der horizontalen Regel. |
| [get_Color](./get_color/)() | Liest oder setzt die Pinsel‑Farbe, die die horizontale Regel füllt. |
| [get_Height](./get_height/)() | Liest oder setzt die Höhe der horizontalen Regel. |
| [get_NoShade](./get_noshade/)() | Gibt an, ob eine 3D‑Schattierung für die horizontale Regel vorhanden ist. Wenn **true**, dann hat die horizontale Regel keine 3D‑Schattierung und es wird eine Vollfarbe verwendet. |
| [get_WidthPercent](./get_widthpercent/)() | Liest oder setzt die Länge der angegebenen horizontalen Regel, ausgedrückt als Prozentsatz der Fensterbreite. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::Drawing::HorizontalRuleAlignment) | Setter für [Aspose::Words::Drawing::HorizontalRuleFormat::get_Alignment](./get_alignment/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter für [Aspose::Words::Drawing::HorizontalRuleFormat::get_Color](./get_color/). |
| [set_Height](./set_height/)(double) | Setter für [Aspose::Words::Drawing::HorizontalRuleFormat::get_Height](./get_height/). |
| [set_NoShade](./set_noshade/)(bool) | Setter für [Aspose::Words::Drawing::HorizontalRuleFormat::get_NoShade](./get_noshade/). |
| [set_WidthPercent](./set_widthpercent/)(double) | Setter für [Aspose::Words::Drawing::HorizontalRuleFormat::get_WidthPercent](./get_widthpercent/). |
| static [Type](./type/)() |  |

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
