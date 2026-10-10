---
title: "Aspose::Words::Drawing::ImageData::get_ImageSize method"
linktitle: "get_ImageSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ImageData::get_ImageSize method. Ottiene le informazioni sulla dimensione e sulla risoluzione dell'immagine in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.drawing/imagedata/get_imagesize/
---
## ImageData::get_ImageSize method


Ottiene le informazioni sulla dimensione e sulla risoluzione dell'immagine.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ImageSize> Aspose::Words::Drawing::ImageData::get_ImageSize()
```

## Note


Se l'immagine è solo collegata e non memorizzata nel documento, restituisce dimensione zero.

## Esempi



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

* Class [ImageSize](../../imagesize/)
* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
