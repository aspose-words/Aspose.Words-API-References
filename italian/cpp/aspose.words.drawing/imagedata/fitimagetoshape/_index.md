---
title: "Aspose::Words::Drawing::ImageData::FitImageToShape metodo"
linktitle: "FitImageToShape"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ImageData::FitImageToShape metodo. Adatta i dati immagine al riquadro della Forma in modo che il rapporto d'aspetto dei dati immagine corrisponda al rapporto d'aspetto del riquadro della Forma in C++."
type: docs
weight: 1500
url: /it/cpp/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData::FitImageToShape method


Adatta i dati immagine al riquadro di [Shape](../../shape/) in modo che il rapporto d'aspetto dei dati immagine corrisponda al rapporto d'aspetto del riquadro di [Shape](../../shape/).

```cpp
void Aspose::Words::Drawing::ImageData::FitImageToShape()
```


## Esempi



Mostra come adattare i dati immagine al riquadro di [Shape](../../shape/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una forma immagine e mantieni la sua orientazione nello stato predefinito.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 300, 450);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Barcode.png");
shape->get_ImageData()->FitImageToShape();

doc->Save(get_ArtifactsDir() + u"Shape.FitImageToShape.docx");
```

## Vedi anche

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
