---
title: Aspose::Words::Drawing::GlowFormat::set_Color method
linktitle: set_Color
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::GlowFormat::set_Color method. Sets a Color object that represents the color for a glow effect. The default value is Black in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.drawing/glowformat/set_color/
---
## GlowFormat::set_Color method


Sets a Color object that represents the color for a glow effect. The default value is Black.

```cpp
void Aspose::Words::Drawing::GlowFormat::set_Color(System::Drawing::Color value)
```

## Examples


Shows how to interact with glow shape effect.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Various shapes.docx"));
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));

shape->get_Glow()->set_Color(System::Drawing::Color::get_Salmon());
shape->get_Glow()->set_Radius(30);
shape->get_Glow()->set_Transparency(0.15);

doc->Save(get_ArtifactsDir() + u"Shape.Glow.docx");

doc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"Shape.Glow.docx"));
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));

ASSERT_EQ(shape->get_Glow()->get_Color().ToArgb(), System::Drawing::Color::FromArgb(217, 250, 128, 114).ToArgb());
ASPOSE_ASSERT_EQ(shape->get_Glow()->get_Radius(), 30);
ASSERT_NEAR(shape->get_Glow()->get_Transparency(), 0.15, 0.01);

shape->get_Glow()->Remove();

ASSERT_EQ(shape->get_Glow()->get_Color().ToArgb(), System::Drawing::Color::get_Black().ToArgb());
ASPOSE_ASSERT_EQ(shape->get_Glow()->get_Radius(), 0);
ASPOSE_ASSERT_EQ(shape->get_Glow()->get_Transparency(), 0);
```
## See Also

* Class [GlowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
