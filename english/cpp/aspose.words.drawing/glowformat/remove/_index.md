---
title: Aspose::Words::Drawing::GlowFormat::Remove method
linktitle: Remove
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::GlowFormat::Remove method. Removes GlowFormat from the parent object in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.drawing/glowformat/remove/
---
## GlowFormat::Remove method


Removes [GlowFormat](../) from the parent object.

```cpp
void Aspose::Words::Drawing::GlowFormat::Remove()
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
