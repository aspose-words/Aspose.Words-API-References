---
title: "Aspose::Words::Drawing::Fill::TwoColorGradient Methode"
linktitle: "TwoColorGradient"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Fill::TwoColorGradient Methode. Setzt die angegebene Füllung auf einen zweifarbigen Farbverlauf in C++."
type: docs
weight: 44000
url: /de/cpp/aspose.words.drawing/fill/twocolorgradient/
---
## Fill::TwoColorGradient(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) method


Setzt die angegebene Füllung auf einen Zweifarbverlauf.

```cpp
void Aspose::Words::Drawing::Fill::TwoColorGradient(Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| style | Aspose::Words::Drawing::GradientStyle | Der Gradientstil [GradientStyle](../../gradientstyle/). |
| variant | Aspose::Words::Drawing::GradientVariant | Die Gradientvariante [GradientVariant](../../gradientvariant/) |

## Beispiele



Zeigt, wie man eine Form mit Farbverläufen füllt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Wendet eine einfarbige Farbverlauf-Füllung auf die Form mit der Vordergrundfarbe des Farbverlaufs an.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Wendet eine zweifarbige Farbverlauf-Füllung auf die Form an.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Ändere die Hintergrundfarbe der Farbverlauf-Füllung.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Beachte, dass Änderungen an \"GradientAngle\" für \"GradientStyle.FromCorner/GradientStyle.FromCenter\"
// Farbverlauf-Füllung hat keine Wirkung, sie funktioniert nur für lineare Farbverläufe.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Verwende die Compliance-Option, um die Form mit DML zu definieren, wenn du \"GradientStyle\" erhalten möchtest,
// \"GradientVariant\" und \"GradientAngle\" Eigenschaften nach dem Speichern des Dokuments.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## Siehe auch

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::TwoColorGradient(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) method


Setzt die angegebene Füllung auf einen Zweifarbverlauf.

```cpp
void Aspose::Words::Drawing::Fill::TwoColorGradient(System::Drawing::Color color1, System::Drawing::Color color2, Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| color1 | System::Drawing::Color | Die erste Farbe zum Erstellen des Farbverlaufs. |
| color2 | System::Drawing::Color | Die zweite Farbe zum Erstellen des Farbverlaufs. |
| style | Aspose::Words::Drawing::GradientStyle | Der Gradientstil [GradientStyle](../../gradientstyle/). |
| variant | Aspose::Words::Drawing::GradientVariant | Die Gradientvariante [GradientVariant](../../gradientvariant/) |

## Beispiele



Zeigt, wie man eine Form mit Farbverläufen füllt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Wendet eine einfarbige Farbverlauf-Füllung auf die Form mit der Vordergrundfarbe des Farbverlaufs an.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Wendet eine zweifarbige Farbverlauf-Füllung auf die Form an.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Ändere die Hintergrundfarbe der Farbverlauf-Füllung.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Beachte, dass Änderungen an \"GradientAngle\" für \"GradientStyle.FromCorner/GradientStyle.FromCenter\"
// Farbverlauf-Füllung hat keine Wirkung, sie funktioniert nur für lineare Farbverläufe.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Verwende die Compliance-Option, um die Form mit DML zu definieren, wenn du \"GradientStyle\" erhalten möchtest,
// \"GradientVariant\" und \"GradientAngle\" Eigenschaften nach dem Speichern des Dokuments.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## Siehe auch

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
