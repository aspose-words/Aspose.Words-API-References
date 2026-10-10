---
title: "Aspose::Words::Drawing::ShapeBase::get_Rotation yöntemi"
linktitle: "get_Rotation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_Rotation yöntemi. Bir şeklin döndürüldüğü açıyı (derece cinsinden) tanımlar. Pozitif değer saat yönünde dönüş açısına karşılık gelir C++ içinde."
type: docs
weight: 45000
url: /tr/cpp/aspose.words.drawing/shapebase/get_rotation/
---
## ShapeBase::get_Rotation method


Bir şeklin döndürüldüğü açıyı (derece cinsinden) tanımlar. Pozitif değer saat yönünde dönüş açısına karşılık gelir.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Rotation()
```

## Açıklamalar


Varsayılan değer 0'dır.

## Örnekler



Bir görüntüyü ekleme ve döndürme yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir görüntülü şekil ekleyin.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_TRUE(shape->get_CanHaveImage());
ASSERT_TRUE(shape->get_HasImage());

// Görüntüyü saat yönünde 45 derece döndürün.
shape->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Shape.Rotate.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
