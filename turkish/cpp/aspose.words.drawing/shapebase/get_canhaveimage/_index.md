---
title: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage metodu"
linktitle: "get_CanHaveImage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_CanHaveImage metodu. C++'da şekil türü şeklin bir görüntüye sahip olmasına izin veriyorsa **true** döndürür."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.drawing/shapebase/get_canhaveimage/
---
## ShapeBase::get_CanHaveImage method


Şekil türü şeklin bir görüntüye sahip olmasına izin veriyorsa **true** döndürür.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_CanHaveImage()
```

## Açıklamalar


Microsoft Word'ün görüntüler için özel bir şekil türü olmasına rağmen, Microsoft Word belgelerinde grup şekli dışındaki herhangi bir şeklin görüntüye sahip olabildiği görülmektedir, bu nedenle bu özellik **true** değerini grup şekli dışındaki tüm şekiller için döndürür [GroupShape](../../groupshape/).

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
