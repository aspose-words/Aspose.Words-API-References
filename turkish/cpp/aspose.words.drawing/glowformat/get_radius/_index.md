---
title: "Aspose::Words::Drawing::GlowFormat::get_Radius yöntemi"
linktitle: "get_Radius"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::GlowFormat::get_Radius yöntemi. Parıltı efekti için yarıçap uzunluğunu puan (pt) cinsinden bir double değer olarak alır veya ayarlar. Varsayılan değer C++'da 0.0'dır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing/glowformat/get_radius/
---
## GlowFormat::get_Radius method


Parıltı etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değerini alır veya ayarlar. Varsayılan değer 0.0.

```cpp
double Aspose::Words::Drawing::GlowFormat::get_Radius()
```


## Örnekler



Parıltı şekil etkisiyle nasıl etkileşim kurulacağını gösterir.
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

## Ayrıca Bakınız

* Class [GlowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
