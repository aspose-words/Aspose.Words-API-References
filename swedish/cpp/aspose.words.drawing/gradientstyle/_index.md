---
title: "Aspose::Words::Drawing::GradientStyle enum"
linktitle: "GradientStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::GradientStyle enum. Anger stilen för en gradientfyllning i C++."
type: docs
weight: 24000
url: /sv/cpp/aspose.words.drawing/gradientstyle/
---
## GradientStyle enum


Anger stil för en gradientfyllning.

```cpp
enum class GradientStyle
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | -1 | Ingen gradient. |
| Horisontell | 1 | Gradient som löper horisontellt över ett objekt. |
| Vertikal | 2 | Gradient som löper vertikalt ner längs ett objekt. |
| DiagonalUp | 3 | Diagonal gradient som rör sig från ett nedre hörn upp till motsatt hörn. |
| DiagonalDown | 4 | Diagonal gradient som rör sig från ett övre hörn ner till motsatt hörn. |
| FromCorner | 5 | Gradient som löper från ett hörn till de andra tre hörnen. |
| FromCenter | 6 | Gradient som löper från mitten ut till hörnen. |


## Exempel



Visar hur man fyller en form med gradienter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Applicera enfärgad gradientfyllning på formen med ForeColor för gradientfyllningen.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Applicera tvåfärgad gradientfyllning på formen.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Ändra BackColor för gradientfyllning.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Observera att ändringar av "GradientAngle" för "GradientStyle.FromCorner/GradientStyle.FromCenter"
// gradientfyllning får ingen effekt, den fungerar bara för linjär gradient.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Använd efterlevnadsalternativet för att definiera formen med DML om du vill få "GradientStyle",
// "GradientVariant" och "GradientAngle" egenskaper efter att dokumentet sparas.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
