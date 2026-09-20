---
title: "Aspose::Words::Drawing::ImageData::FitImageToShape método"
linktitle: "FitImageToShape"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageData::FitImageToShape método. Ajusta los datos de imagen al marco de Shape para que la relación de aspecto de los datos de imagen coincida con la relación de aspecto del marco de Shape en C++."
type: docs
weight: 1500
url: /es/cpp/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData::FitImageToShape method


Ajusta los datos de imagen al marco de [Shape](../../shape/) para que la relación de aspecto de los datos de imagen coincida con la relación de aspecto del marco de [Shape](../../shape/).

```cpp
void Aspose::Words::Drawing::ImageData::FitImageToShape()
```


## Ejemplos



Muestra cómo ajustar los datos de imagen al marco de [Shape](../../shape/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una forma de imagen y mantenga su orientación en su estado predeterminado.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 300, 450);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Barcode.png");
shape->get_ImageData()->FitImageToShape();

doc->Save(get_ArtifactsDir() + u"Shape.FitImageToShape.docx");
```

## Ver también

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
