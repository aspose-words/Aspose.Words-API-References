---
title: "Aspose::Words::Drawing::GradientVariant enum"
linktitle: "GradientVariant"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::GradientVariant enum. Anger varianten för en gradientfyllning i C++."
type: docs
weight: 25000
url: /sv/cpp/aspose.words.drawing/gradientvariant/
---
## GradientVariant enum


Anger varianten för en gradientfyllning.

```cpp
enum class GradientVariant
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Gradientvariant 'None'. |
| Variant1 | 1 | Gradientvariant 1. |
| Variant2 | 2 | Gradientvariant 2. |
| Variant3 | 3 | Gradientvariant 3. |
| Variant4 | 4 | Gradientvariant 4. |


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
