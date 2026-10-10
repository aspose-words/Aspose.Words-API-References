---
title: "Aspose::Words::Drawing::ImageData::FitImageToShape طريقة"
linktitle: "FitImageToShape"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ImageData::FitImageToShape طريقة. يضبط بيانات الصورة لتتناسب مع إطار الشكل بحيث تتطابق نسبة العرض إلى الارتفاع لبيانات الصورة مع نسبة العرض إلى الارتفاع لإطار الشكل في C++."
type: docs
weight: 1500
url: /ar/cpp/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData::FitImageToShape method


يضبط بيانات الصورة إلى إطار [Shape](../../shape/) بحيث تتطابق نسبة العرض إلى الارتفاع لبيانات الصورة مع نسبة العرض إلى الارتفاع لإطار [Shape](../../shape/).

```cpp
void Aspose::Words::Drawing::ImageData::FitImageToShape()
```


## أمثلة



يعرض كيفية ضبط بيانات الصورة لتتناسب مع إطار [Shape](../../shape/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج شكلاً صورة واترك توجيهه في حالته الافتراضية.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 300, 450);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Barcode.png");
shape->get_ImageData()->FitImageToShape();

doc->Save(get_ArtifactsDir() + u"Shape.FitImageToShape.docx");
```

## انظر أيضًا

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
