---
title: "Aspose::Words::Drawing::ImageData::FitImageToShape metodu"
linktitle: "FitImageToShape"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ImageData::FitImageToShape metodu. Görüntü verisini Shape çerçevesine sığdırır, böylece görüntü verisinin en‑boy oranı Shape çerçevesinin en‑boy oranına C++'ta eşleşir."
type: docs
weight: 1500
url: /tr/cpp/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData::FitImageToShape method


Görüntü verisini [Shape](../../shape/) çerçevesine sığdırır, böylece görüntü verisinin en‑boy oranı [Shape](../../shape/) çerçevesinin en‑boy oranına eşleşir.

```cpp
void Aspose::Words::Drawing::ImageData::FitImageToShape()
```


## Örnekler



Görüntü verisini [Shape](../../shape/) çerçevesine nasıl sığdırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir resim şekli ekleyin ve yönelimini varsayılan durumunda bırakın.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 300, 450);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Barcode.png");
shape->get_ImageData()->FitImageToShape();

doc->Save(get_ArtifactsDir() + u"Shape.FitImageToShape.docx");
```

## Ayrıca Bakınız

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
