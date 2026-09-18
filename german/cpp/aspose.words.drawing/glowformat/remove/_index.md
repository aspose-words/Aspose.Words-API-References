---
title: "Aspose::Words::Drawing::GlowFormat::Remove Methode"
linktitle: "Remove"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::GlowFormat::Remove Methode. Entfernt GlowFormat aus dem übergeordneten Objekt in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.drawing/glowformat/remove/
---
## GlowFormat::Remove method


Entfernt [GlowFormat](../) aus dem übergeordneten Objekt.

```cpp
void Aspose::Words::Drawing::GlowFormat::Remove()
```


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

* Class [GlowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
