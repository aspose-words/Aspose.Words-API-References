---
title: "Aspose::Words::Drawing::ShapeBase::get_DistanceTop metodu"
linktitle: "get_DistanceTop"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_DistanceTop metodu. C++'ta belge metni ile şeklin üst kenarı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.drawing/shapebase/get_distancetop/
---
## ShapeBase::get_DistanceTop method


Belge metni ile şeklin üst kenarı arasındaki mesafeyi (nokta cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_DistanceTop()
```

## Açıklamalar


Varsayılan değer 0'dır.

Yalnızca üst düzey şekiller için etkilidir.

## Örnekler



Bir şekli çevreleyen metnin sarma mesafesini nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir dikdörtgen ekleyin ve metnin onun sınırları etrafında sıkı bir şekilde sarılmasını sağlayın.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 150, 150);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Tight);

// Şekil ile çevresindeki metin arasındaki minimum mesafeyi tüm kenarlardan 40pt olarak ayarlayın.
shape->set_DistanceTop(40);
shape->set_DistanceBottom(40);
shape->set_DistanceLeft(40);
shape->set_DistanceRight(40);

// Şekli sayfanın ortasına daha yakın bir konuma taşıyın ve ardından şekli saat yönünde 60 derece döndürün.
shape->set_Top(75);
shape->set_Left(150);
shape->set_Rotation(60);

// Şeklin etrafında sarılacak bir metin ekleyin.
builder->get_Font()->set_Size(24);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"Shape.Coordinates.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
