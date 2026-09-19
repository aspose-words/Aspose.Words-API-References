---
title: "Aspose::Words::Drawing::FlipOrientation enum"
linktitle: "FlipOrientation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::FlipOrientation enum. Possibili valori per l'orientamento di una forma in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words.drawing/fliporientation/
---
## FlipOrientation enum


Valori possibili per l'orientamento di una forma.

```cpp
enum class FlipOrientation
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Le coordinate non sono capovolte. |
| Orizzontale | 1 | Capovolgi lungo l'asse y, invertendo le coordinate x. |
| Verticale | 2 | Capovolgi lungo l'asse x, invertendo le coordinate y. |
| Entrambi | 3 | Capovolgi lungo entrambi gli assi y e x. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
