---
title: "Aspose::Words::Drawing::ImageData::FitImageToShape metod"
linktitle: "FitImageToShape"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ImageData::FitImageToShape metod. Anpassar bilddata till Shape-ramen så att bildförhållandet för bilddata matchar bildförhållandet för Shape-ramen i C++."
type: docs
weight: 1500
url: /sv/cpp/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData::FitImageToShape method


Anpassar bilddata till [Shape](../../shape/) ram så att bildförhållandet för bilddata matchar bildförhållandet för [Shape](../../shape/) ram.

```cpp
void Aspose::Words::Drawing::ImageData::FitImageToShape()
```


## Exempel



Visar hur man anpassar bilddata till [Shape](../../shape/) ram.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en bildform och låt dess orientering vara i standardläget.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 300, 450);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Barcode.png");
shape->get_ImageData()->FitImageToShape();

doc->Save(get_ArtifactsDir() + u"Shape.FitImageToShape.docx");
```

## Se även

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
