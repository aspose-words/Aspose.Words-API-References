---
title: "Aspose::Words::Drawing::GlowFormat class"
linktitle: "GlowFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::GlowFormat Klasse. Stellt die Leuchteformatierung für ein Objekt in C++ dar."
type: docs
weight: 1500
url: /de/cpp/aspose.words.drawing/glowformat/
---
## GlowFormat class


Stellt die Leuchteffekt-Formatierung für ein Objekt dar.

```cpp
class GlowFormat : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Color](./get_color/)() | Liest oder setzt ein **Color**-Objekt, das die Farbe für einen Leuchteeffekt darstellt. Der Standardwert ist **Black**. |
| [get_Radius](./get_radius/)() | Liest oder setzt einen double-Wert, der die Länge des Radius für einen Leuchteeffekt in Punkten (pt) darstellt. Der Standardwert ist 0.0. |
| [get_Transparency](./get_transparency/)() | Liest oder setzt den Transparenzgrad für den Leuchteeffekt als Wert zwischen 0.0 (undurchsichtig) und 1.0 (klar). Der Standardwert ist 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Entfernt [GlowFormat](./) aus dem übergeordneten Objekt. |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter für [Aspose::Words::Drawing::GlowFormat::get_Color](./get_color/). |
| [set_Radius](./set_radius/)(double) | Setter für [Aspose::Words::Drawing::GlowFormat::get_Radius](./get_radius/). |
| [set_Transparency](./set_transparency/)(double) | Setter für [Aspose::Words::Drawing::GlowFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Hinweise


Verwenden Sie die Eigenschaft [Glow](../shapebase/get_glow/), um auf die Leuchte‑Eigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der Klasse [GlowFormat](./) direkt.

## Beispiele



Zeigt, wie man mit dem Leuchte‑Formeffekt interagiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Glow()->set_Color(System::Drawing::Color::get_Salmon());
shape->get_Glow()->set_Radius(30);
shape->get_Glow()->set_Transparency(0.15);

doc->Save(get_ArtifactsDir() + u"Shape.Glow.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Glow.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::Drawing::Color::FromArgb(217, 250, 128, 114).ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(30, shape->get_Glow()->get_Radius());
ASSERT_NEAR(0.15, shape->get_Glow()->get_Transparency(), 0.01);

shape->get_Glow()->Remove();

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Radius());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Transparency());
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
