---
title: Aspose::Words::Drawing::ImageData::FitImageToShape method
linktitle: FitImageToShape
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ImageData::FitImageToShape method. Fits the image data to Shape frame so that the aspect ratio of the image data matches the aspect ratio of Shape frame in C++.'
type: docs
weight: 1500
url: /cpp/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData::FitImageToShape method


Fits the image data to [Shape](../../shape/) frame so that the aspect ratio of the image data matches the aspect ratio of [Shape](../../shape/) frame.

```cpp
void Aspose::Words::Drawing::ImageData::FitImageToShape()
```


## Examples



Shows hot to fit the image data to [Shape](../../shape/) frame. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert an image shape and leave its orientation in its default state.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 300, 450);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Barcode.png");
shape->get_ImageData()->FitImageToShape();

doc->Save(get_ArtifactsDir() + u"Shape.FitImageToShape.docx");
```

## See Also

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
