---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_Glow"
linktitle: "get_Glow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_Glow. Ottiene la formattazione di bagliore per la forma in C++."
type: docs
weight: 21500
url: /it/cpp/aspose.words.drawing/shapebase/get_glow/
---
## ShapeBase::get_Glow method


Ottiene la formattazione dell'effetto bagliore per la forma.

```cpp
System::SharedPtr<Aspose::Words::Drawing::GlowFormat> Aspose::Words::Drawing::ShapeBase::get_Glow()
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

* Class [GlowFormat](../../glowformat/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
