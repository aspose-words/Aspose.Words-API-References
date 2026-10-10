---
title: "Aspose::Words::Drawing::ImageData::FitImageToShape-Methode"
linktitle: "FitImageToShape"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageData::FitImageToShape-Methode. Passt die Bilddaten an den Shape-Rahmen an, sodass das Seitenverhältnis der Bilddaten dem Seitenverhältnis des Shape-Rahmens in C++ entspricht."
type: docs
weight: 1500
url: /de/cpp/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData::FitImageToShape method


Passt die Bilddaten an den [Shape](../../shape/)-Rahmen an, sodass das Seitenverhältnis der Bilddaten dem Seitenverhältnis des [Shape](../../shape/)-Rahmens entspricht.

```cpp
void Aspose::Words::Drawing::ImageData::FitImageToShape()
```


## Beispiele



Zeigt, wie man die Bilddaten an den [Shape](../../shape/)-Rahmen anpasst.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Bildform ein und belassen Sie ihre Ausrichtung im Standardzustand.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 300, 450);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Barcode.png");
shape->get_ImageData()->FitImageToShape();

doc->Save(get_ArtifactsDir() + u"Shape.FitImageToShape.docx");
```

## Siehe auch

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
