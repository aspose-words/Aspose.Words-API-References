---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_Height"
linktitle: "get_Height"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_Height. Ottiene o imposta l'altezza del blocco contenitore della forma in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.drawing/shapebase/get_height/
---
## ShapeBase::get_Height method


Ottiene o imposta l'altezza del blocco contenitore della forma.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Height()
```

## Note


Per una forma di livello superiore, il valore è in punti.

Per le forme in un gruppo, il valore è nello spazio delle coordinate e nelle unità del gruppo genitore.

Il valore predefinito è 0.

## Esempi



Mostra come inserire un'immagine flottante e specificarne la posizione e le dimensioni.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Configura la proprietà "RelativeHorizontalPosition" della forma per trattare il valore della proprietà "Left"
// come distanza orizzontale della forma, in punti, dal lato sinistro della pagina.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Imposta la distanza orizzontale della forma dal lato sinistro della pagina a 100.
shape->set_Left(100);

// Usa la proprietà "RelativeVerticalPosition" in modo simile per posizionare la forma 80pt sotto la parte superiore della pagina.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Imposta l'altezza della forma, che scalerà automaticamente la larghezza per preservare le dimensioni.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Le proprietà "Bottom" e "Right" contengono i bordi inferiore e destro dell'immagine.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```


Mostra come ridimensionare una forma con un'immagine.
```cpp
// Quando inseriamo un'immagine usando il metodo "InsertImage", il costruttore scala la forma che visualizza l'immagine in modo che,
// quando visualizziamo il documento con zoom al 100% in Microsoft Word, la forma mostra l'immagine nella sua dimensione reale.
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Un'immagine 400x400 creerà un oggetto ImageData con una dimensione dell'immagine di 300x300pt.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Se le dimensioni di una forma corrispondono alle dimensioni dei dati dell'immagine,
// allora la forma visualizza l'immagine nella sua dimensione originale.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// Riduci la dimensione complessiva della forma del 50%.
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

// I fattori di scala si applicano sia alla larghezza che all'altezza contemporaneamente per preservare le proporzioni della forma.
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// Quando ridimensioniamo la forma, la dimensione dei dati dell'immagine rimane invariata.
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Possiamo fare riferimento alle dimensioni dei dati dell'immagine per applicare una scala basata sulla dimensione dell'immagine.
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
