---
title: "metodo Aspose::Words::Drawing::Fill::TwoColorGradient"
linktitle: "TwoColorGradient"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Drawing::Fill::TwoColorGradient. Imposta il riempimento specificato a un gradiente a due colori in C++."
type: docs
weight: 44000
url: /it/cpp/aspose.words.drawing/fill/twocolorgradient/
---
## Fill::TwoColorGradient(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) method


Imposta il riempimento specificato su una sfumatura a due colori.

```cpp
void Aspose::Words::Drawing::Fill::TwoColorGradient(Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| style | Aspose::Words::Drawing::GradientStyle | Lo stile di gradiente [GradientStyle](../../gradientstyle/). |
| variant | Aspose::Words::Drawing::GradientVariant | La variante del gradiente [GradientVariant](../../gradientvariant/) |

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

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::TwoColorGradient(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) method


Imposta il riempimento specificato su una sfumatura a due colori.

```cpp
void Aspose::Words::Drawing::Fill::TwoColorGradient(System::Drawing::Color color1, System::Drawing::Color color2, Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| color1 | System::Drawing::Color | Il primo colore per creare il gradiente. |
| color2 | System::Drawing::Color | Il secondo colore per creare il gradiente. |
| style | Aspose::Words::Drawing::GradientStyle | Lo stile di gradiente [GradientStyle](../../gradientstyle/). |
| variant | Aspose::Words::Drawing::GradientVariant | La variante del gradiente [GradientVariant](../../gradientvariant/) |

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

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
