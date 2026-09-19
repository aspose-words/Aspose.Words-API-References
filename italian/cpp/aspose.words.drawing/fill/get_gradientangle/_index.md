---
title: "Aspose::Words::Drawing::Fill::get_GradientAngle metodo"
linktitle: "get_GradientAngle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Fill::get_GradientAngle metodo. Ottiene o imposta l'angolo del riempimento gradiente in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.drawing/fill/get_gradientangle/
---
## Fill::get_GradientAngle method


Ottiene o imposta l'angolo del riempimento gradiente.

```cpp
double Aspose::Words::Drawing::Fill::get_GradientAngle()
```


## Esempi



Mostra come riempire una forma con dei gradienti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Applica un riempimento a gradiente monocolore alla forma con il ForeColor del gradiente.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Applica un riempimento a gradiente bicolore alla forma.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Modifica il BackColor del riempimento a gradiente.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Nota che le modifiche a "GradientAngle" per "GradientStyle.FromCorner/GradientStyle.FromCenter"
// Il riempimento a gradiente non ha alcun effetto, funzionerà solo per i gradienti lineari.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Usa l'opzione di conformità per definire la forma usando DML se vuoi ottenere "GradientStyle",
// "GradientVariant" e le proprietà "GradientAngle" dopo il salvataggio del documento.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## Vedi anche

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
