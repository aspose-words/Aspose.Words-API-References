---
title: "Aspose::Words::Drawing::GlowFormat::get_Radius metod"
linktitle: "get_Radius"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::GlowFormat::get_Radius metod. Hämtar eller anger ett dubbelvärde som representerar radielängden för en glödeffekt i punkter (pt). Standardvärdet är 0,0 i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.drawing/glowformat/get_radius/
---
## GlowFormat::get_Radius method


Hämtar eller anger ett double‑värde som representerar radie‑längden för en glödeffekt i punkter (pt). Standardvärdet är 0.0.

```cpp
double Aspose::Words::Drawing::GlowFormat::get_Radius()
```


## Exempel



Visar hur man interagerar med glödeffekten för en form.
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

## Se även

* Class [GlowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
