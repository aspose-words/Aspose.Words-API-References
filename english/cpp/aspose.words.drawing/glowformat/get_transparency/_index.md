---
title: Aspose::Words::Drawing::GlowFormat::get_Transparency method
linktitle: get_Transparency
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::GlowFormat::get_Transparency method. Gets or sets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0 in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.drawing/glowformat/get_transparency/
---
## GlowFormat::get_Transparency method


Gets or sets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0.

```cpp
double Aspose::Words::Drawing::GlowFormat::get_Transparency()
```


## Examples



Shows how to interact with glow shape effect. 
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

## See Also

* Class [GlowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
