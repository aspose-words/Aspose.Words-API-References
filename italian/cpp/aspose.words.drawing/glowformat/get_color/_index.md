---
title: "Metodo Aspose::Words::Drawing::GlowFormat::get_Color"
linktitle: "get_Color"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::GlowFormat::get_Color. Ottiene o imposta un oggetto Color che rappresenta il colore per un effetto bagliore. Il valore predefinito è Black in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing/glowformat/get_color/
---
## GlowFormat::get_Color method


Ottiene o imposta un oggetto **Color** che rappresenta il colore per un effetto di bagliore. Il valore predefinito è **Black**.

```cpp
System::Drawing::Color Aspose::Words::Drawing::GlowFormat::get_Color()
```


## Esempi



Mostra come interagire con l'effetto di forma di bagliore.
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

## Vedi anche

* Class [GlowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
