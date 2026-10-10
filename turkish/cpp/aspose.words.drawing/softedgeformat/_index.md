---
title: "Aspose::Words::Drawing::SoftEdgeFormat class"
linktitle: "SoftEdgeFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::SoftEdgeFormat class. C++'da bir nesne için yumuşak kenar biçimlendirmesini temsil eder."
type: docs
weight: 13500
url: /tr/cpp/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class


Bir nesne için yumuşak kenar biçimlendirmesini temsil eder.

```cpp
class SoftEdgeFormat : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Radius](./get_radius/)() | Yumuşak kenar etkisi için yarıçap uzunluğunu puan (pt) cinsinden temsil eden çift (double) bir değeri alır veya ayarlar. Varsayılan değer 0.0'dır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Üst nesneden [SoftEdgeFormat](./) öğesini kaldırır. |
| [set_Radius](./set_radius/)(double) | [Aspose::Words::Drawing::SoftEdgeFormat::get_Radius](./get_radius/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir nesnenin yumuşak kenar özelliklerine erişmek için [SoftEdge](../shapebase/get_softedge/) özelliğini kullanın. [SoftEdgeFormat](./) sınıfının örneklerini doğrudan oluşturmazsınız.

## Örnekler



Yumuşak kenar biçimlendirmesiyle nasıl çalışılacağını gösterir.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 200);

// Şekle yumuşak kenar uygula.
shape->get_SoftEdge()->set_Radius(30);

builder->get_Document()->Save(get_ArtifactsDir() + u"Shape.SoftEdge.docx");

// Yumuşak kenarlı dikdörtgen şekilli belgeyi yükle.
auto doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.SoftEdge.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::SoftEdgeFormat> softEdgeFormat = shape->get_SoftEdge();

// Yumuşak kenar yarıçapını kontrol et.
ASPOSE_ASSERT_EQ(30, softEdgeFormat->get_Radius());

// Şekilden yumuşak kenarı kaldır.
softEdgeFormat->Remove();

// Kaldırılan yumuşak kenarın yarıçapını kontrol edin.
ASPOSE_ASSERT_EQ(0, softEdgeFormat->get_Radius());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
