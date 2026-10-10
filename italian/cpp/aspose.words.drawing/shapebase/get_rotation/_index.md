---
title: "Aspose::Words::Drawing::ShapeBase::get_Rotation metodo"
linktitle: "get_Rotation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Rotation metodo. Definisce l'angolo (in gradi) di rotazione di una shape. Un valore positivo corrisponde all'angolo di rotazione in senso orario in C++."
type: docs
weight: 45000
url: /it/cpp/aspose.words.drawing/shapebase/get_rotation/
---
## ShapeBase::get_Rotation method


Definisce l'angolo (in gradi) di rotazione di una forma. Un valore positivo corrisponde all'angolo di rotazione in senso orario.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Rotation()
```

## Note


Il valore predefinito è 0.

## Esempi



Mostra come inserire e ruotare un'immagine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una forma con un'immagine.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Ruota l'immagine di 45 gradi in senso orario.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
