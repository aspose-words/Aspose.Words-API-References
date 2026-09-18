---
title: "Aspose::Words::Drawing::ShadowFormat class"
linktitle: "ShadowFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShadowFormat class. Stellt die Schattenformatierung für ein Objekt dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.drawing/shadowformat/
---
## ShadowFormat class


Stellt die Schattenformatierung für ein Objekt dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class ShadowFormat : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clear](./clear/)() | Löscht die Schattenformatierung. |
| [get_Color](./get_color/)() | Liest oder setzt ein **Color**‑Objekt, das die Farbe des Schattens darstellt. Der Standardwert ist **Black**. |
| [get_Transparency](./get_transparency/)() | Liest oder setzt den Transparenzgrad für den Schatteneffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (transparent). Der Standardwert ist 0.0. |
| [get_Type](./get_type/)() | Liest oder setzt den angegebenen [ShadowType](../shadowtype/) für [ShadowFormat](./). |
| [get_Visible](./get_visible/)() | Gibt **true** zurück, wenn die auf diese Instanz angewendete Formatierung sichtbar ist. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter für [Aspose::Words::Drawing::ShadowFormat::get_Color](./get_color/). |
| [set_Transparency](./set_transparency/)(double) | Setter für [Aspose::Words::Drawing::ShadowFormat::get_Transparency](./get_transparency/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::ShadowType) | Setter für [Aspose::Words::Drawing::ShadowFormat::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man die Schattenfarbe abruft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
