---
title: "Aspose::Words::Drawing::GlowFormat classe"
linktitle: "GlowFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::GlowFormat classe. Rappresenta la formattazione di bagliore per un oggetto in C++."
type: docs
weight: 1500
url: /it/cpp/aspose.words.drawing/glowformat/
---
## GlowFormat class


Rappresenta la formattazione dell'effetto bagliore per un oggetto.

```cpp
class GlowFormat : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Color](./get_color/)() | Ottiene o imposta un oggetto **Color** che rappresenta il colore per un effetto di bagliore. Il valore predefinito è **Black**. |
| [get_Radius](./get_radius/)() | Ottiene o imposta un valore double che rappresenta la lunghezza del raggio per un effetto di bagliore in punti (pt). Il valore predefinito è 0.0. |
| [get_Transparency](./get_transparency/)() | Ottiene o imposta il grado di trasparenza per l'effetto di bagliore come valore compreso tra 0.0 (opaco) e 1.0 (chiaro). Il valore predefinito è 0.0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Rimuove [GlowFormat](./) dall'oggetto padre. |
| [set_Color](./set_color/)(System::Drawing::Color) | Metodo set per [Aspose::Words::Drawing::GlowFormat::get_Color](./get_color/). |
| [set_Radius](./set_radius/)(double) | Metodo set per [Aspose::Words::Drawing::GlowFormat::get_Radius](./get_radius/). |
| [set_Transparency](./set_transparency/)(double) | Metodo set per [Aspose::Words::Drawing::GlowFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Note


Usa la proprietà [Glow](../shapebase/get_glow/) per accedere alle proprietà di bagliore di un oggetto. Non crei istanze della classe [GlowFormat](./) direttamente.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
