---
title: "Aspose::Words::Drawing::Fill::get_GradientAngle-Methode"
linktitle: "get_GradientAngle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Fill::get_GradientAngle-Methode. Ruft den Winkel der Farbverlauffüllung ab oder legt ihn fest in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.drawing/fill/get_gradientangle/
---
## Fill::get_GradientAngle method


Liest oder legt den Winkel der Farbverlauf-Füllung fest.

```cpp
double Aspose::Words::Drawing::Fill::get_GradientAngle()
```


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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
