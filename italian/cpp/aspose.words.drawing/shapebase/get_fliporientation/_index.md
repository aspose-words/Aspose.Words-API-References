---
title: "Aspose::Words::Drawing::ShapeBase::get_FlipOrientation metodo"
linktitle: "get_FlipOrientation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_FlipOrientation metodo. Cambia l'orientamento di una forma in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words.drawing/shapebase/get_fliporientation/
---
## ShapeBase::get_FlipOrientation method


Cambia l'orientamento di una forma.

```cpp
Aspose::Words::Drawing::FlipOrientation Aspose::Words::Drawing::ShapeBase::get_FlipOrientation()
```

## Note


Il valore predefinito è [None](../../fliporientation/).

## Esempi



Mostra come capovolgere una forma su un asse.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una forma immagine e mantieni la sua orientazione nello stato predefinito.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Imposta la proprietà \"FlipOrientation\" su \"FlipOrientation.Horizontal\" per capovolgere la seconda forma sull'asse y,
// trasformandola in un'immagine speculare orizzontale della prima forma.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Horizontal);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Imposta la proprietà \"FlipOrientation\" su \"FlipOrientation.Horizontal\" per capovolgere la terza forma sull'asse x,
// trasformandola in un'immagine speculare verticale della prima forma.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Vertical);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Imposta la proprietà \"FlipOrientation\" su \"FlipOrientation.Horizontal\" per capovolgere la quarta forma su entrambi gli assi x e y,
// trasformandola in un'immagine speculare orizzontale e verticale della prima forma.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Both);

doc->Save(get_ArtifactsDir() + u"Shape.FlipShapeOrientation.docx");
```

## Vedi anche

* Enum [FlipOrientation](../../fliporientation/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
