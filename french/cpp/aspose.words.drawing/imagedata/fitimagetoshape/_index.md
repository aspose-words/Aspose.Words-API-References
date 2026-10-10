---
title: "Aspose::Words::Drawing::ImageData::FitImageToShape method"
linktitle: "FitImageToShape"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageData::FitImageToShape method. Ajuste les données d'image au cadre de la forme afin que le rapport d'aspect des données d'image corresponde au rapport d'aspect du cadre de la forme en C++."
type: docs
weight: 1500
url: /fr/cpp/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData::FitImageToShape method


Ajuste les données d'image au cadre de [Shape](../../shape/) afin que le rapport d'aspect des données d'image corresponde au rapport d'aspect du cadre de [Shape](../../shape/).

```cpp
void Aspose::Words::Drawing::ImageData::FitImageToShape()
```


## Exemples



Montre comment ajuster les données d'image au cadre de [Shape](../../shape/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une forme d'image et laissez son orientation dans son état par défaut.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 300, 450);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Barcode.png");
shape->get_ImageData()->FitImageToShape();

doc->Save(get_ArtifactsDir() + u"Shape.FitImageToShape.docx");
```

## Voir aussi

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
